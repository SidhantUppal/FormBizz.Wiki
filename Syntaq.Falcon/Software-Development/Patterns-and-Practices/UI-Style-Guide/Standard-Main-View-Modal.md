**Standard Index View**

![image.png](/.attachments/image-515d6222-a7fc-431c-a61c-6d96cd4d3685.png)

**HTML By Component**

1. Header
`<abp-page-subheader title="@L("Users")" description="@L("UsersHeaderInfo")">`

2. Create Button
`            <button id="CreateNewUserButton" class="btn btn-primary">
                <i class="fa fa-plus btn-md-icon"></i>
                <span class="d-none d-md-inline-block">
                    @L("CreateNewUser")
                </span>
            </button>`

3. Search
`<div class="input-group">
                                    <input type="text" id="UsersTableFilter" class="form-control" placeholder="@L("SearchWithThreeDot")" value="@Model.FilterText">
                                    <button class="btn btn-secondary" id="clearbtn" type="button">
                                        <i class="fas fa-times"></i>
                                    </button>
                                    <button id="GetUsersButton" class="btn btn-primary" type="submit">
                                        <i class="flaticon-search-1" aria-label="@L("Search")"></i>
                                    </button>
                                </div>`
  4. Advanced Filters
`<div id="AdvacedAuditFiltersArea" style="display: none" class="row mb-4">
                        <div class="@(IsGranted(AppPermissions.Pages_Administration_Roles) ? "col-xl-6" : "col-xl-12")">
                            <div class="mb-5">
                                <button class="btn btn-secondary w-100" id="FilterByPermissionsButton">@L("SelectPermissions") (<span id="NumberOfFilteredPermission">0</span>)</button>
                            </div>
                        </div>
                        <div class="col-xl-12 text-end">
                            <button id="RefreshUserListButton" class="btn btn-primary float-end">
                                <i class="fa fa-sync btn-md-icon"></i> 
                                <span class="d-none d-md-inline-block">
                                    @L("Refresh")
                                </span>
                            </button>
                        </div>
                    </div>
                    <div class="row mb-4">
                        <div class="col-xl-12">
                            <span id="ShowAdvancedFiltersSpan" class="text-muted clickable-item">
                                <i class="fa fa-angle-down"></i> @L("ShowAdvancedFilters")
                            </span>
                            <span id="HideAdvancedFiltersSpan" class="text-muted clickable-item" style="display: none">
                                <i class="fa fa-angle-up"></i> @L("HideAdvancedFilters")
                            </span>
                        </div>
                    </div>`
5. Table
`                <div class="align-items-center">
                    <table id="UsersTable" class="table align-middle table-row-dashed fs-6 gy-5 dataTable no-footer">
                        <thead>
                            <tr>
                                <th></th>
                                <th>@L("Actions")</th>
                                <th>@L("UserName")</th>
                            </tr>
                        </thead>
                    </table>
                </div>`