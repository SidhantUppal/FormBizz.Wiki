
**By Components:**
1. img
- Accessibility error: no alternative text for image
- Solution: add descriptive alt attribute value or "" for decorative images
- Solution sample: `<img alt="Logo" src="/Common/Images/app-logo-on-light.svg" class="header-brand-logo-default h-35px logo">`
2. h1
- Accessibility error: no first-level heading
- Solution: Place page main heading in <h1>	
3. h2...h6
- Accessibility error: heading level skipping		
- Solution: replace <h2...h6> with corresponding classes
- Solution sample: `<span class="modal-title h5">
        <span>Create new user</span>
    </span>`
4. label		
- Accessibility error: attribute **for** value not coherent with corresponding form **id**
- Solution: attribute value of for same as form(input, textarea, etc) id
- Solution sample: 
`<label for="EditUser_Password" class="form-label">Password</label>`
`<input id="EditUser_Password" type="password" name="Password" class="form-control auto-complete-off" onfocus="this.removeAttribute('readonly');" maxlength="32" autocomplete="new-password" required="required">`	
5. label 		
- Accessibility error: label without text
- Solution: add descriptive title attribute value
- Solution sample: `<label title="Customer's First name"></label><br />` 			
6. input			
- Accessibility error: attribute hidden does not support accessibility
- Solution: replace hidden with type="hidden"
- Solution sample: `<input class="form-control" name="selectProjectId" value="b75f19cc-0f90-4244-9ea3-9db03235946b" type="hidden">` 		
7. input
- Accessibility error: no corresponding label	
- Solution: add descriptive attribute aria-label value	
- Solution sample: `<input type="number" aria-label="subscriber number">`
8. button	
- Accessibility error: button no discernible text or no label	
- Solution: add descriptive attribute aria-label value		
- Solution sample: ` <button aria-label="Close" class="close-button"></button>`
9. ul li		 
- Accessibility error: list not accessible via keyboard
- Solution: add keyboard event handler to support keyboard navigation
- Solution sample: `[https://dev.azure.com/syntaqsolutions/Falcon/_git/Syntaq.Falcon/commit/ece721ddf85659fd0736db9937d496b0e22d935c?refName=refs/heads/8981-MBIE-Accessibility-Using-WCAG-2-1&path=/src/Syntaq.Falcon.Web.Mvc/wwwroot/view-resources/Areas/Falcon/Views/Apps/Index.js`
10. td		
- Accessibility error: table not navigatable via tab key
- Solution: add tabindex attribute value
- Solution sample: `https://dev.azure.com/syntaqsolutions/Falcon/_git/Syntaq.Falcon/commit/2d3f6a8a12a8511c1830fe2740a85d2d0f53f4dd?path=/src/Syntaq.Falcon.Web.Mvc/wwwroot/view-resources/Areas/Falcon/Views/CustomizableDashboard/Widgets/WaitingContributor/WaitingContributor.min.js&_a=files`				 
11. focusable div, checkbox, etc		
- Accessibility error: focus not visible
- Solution: add focus/hover css, or tabindex attribute value	
12. All elements		
- Accessibility error: color contrast ratio of background/box and text color less than 4.5
- Solution: adjust background or text color to reach 4.5:1 above	
- Solution sample: `https://contrast-ratio.com`
13. disabled attribute	
- Accessibility error: elements with disabled="" "disabled"
- Solution: just use attribute disabled, without value
- Solution sample: `<button aria-label="Close" class="close-button" disabled></button>`
14. < a > 
- Accessibility error: no text	
- Solution: add descriptive attribute aria-label value	
- Solution sample: `<a target="_blank" aria-label="reload">`
15. < a > 
- Accessibility error: failed to tab through and navigate due to no href atrribute	
- Solution: add href="#"
- Solution sample: `<a target="_blank" aria-label="reload" href="#">`
			

			