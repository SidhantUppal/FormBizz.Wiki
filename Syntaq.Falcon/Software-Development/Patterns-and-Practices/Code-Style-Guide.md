## standards
- naming convention of method:  should not contains 'func'
 
e.g: a method called 'private Boolean containStepsProjectfunc' should be named as 'hasSteps'

- css: avoid use absolute positioning unless no other option.
- Any public method we must check to see if the user is allowed to get the data

 public async Task<GetFormFeedbackForViewDto> GetFormFeedbackForView(Guid id)
         {
            // Feedback form anonymously user
            _unitOfWorkManager.Current.DisableFilter(AbpDataFilters.MayHaveTenant);

 

            ACLResultDto ACLResult = _ACLManager.CheckAccess(new ACLCheckDto() { Action = "View", EntityId = Id, UserId = AbpSession.UserId });
            if (ACLResult.IsAuthed)
            {

 

                var formFeedback = await _formFeedbackRepository.GetAsync(id);
                var feedbackForm = await _lookup_formRepository.GetAsync(formFeedback.FeedbackFormId);

 

                var output = new GetFormFeedbackForViewDto { 
                    FormFeedback = ObjectMapper.Map<FormFeedbackDto>(formFeedback),
                    UserName = formFeedback.UserName,
                    Email = formFeedback.Email,
                    Rating = formFeedback.Rating,
                    Comment = formFeedback.Comment,
                    FeedbackFormSchema = feedbackForm.Schema,
                    FeedbackFormData = formFeedback.FeedbackFormData
                };

 

                if (output.FormFeedback.FormId != null)
                {
                    var _lookupForm = await _lookup_formRepository.FirstOrDefaultAsync((Guid)output.FormFeedback.FormId);
                    output.FormName = _lookupForm?.Name?.ToString();
                }
            
                return output;
            }
            else
            {
                throw new UserFriendlyException("Not Authorised");
            }

 

         }