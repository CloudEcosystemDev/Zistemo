# <p align="center" width="100%"> <img src="./logo.png" width="250" height="250"> </p> 
# <p align="center" width="100%"> Zistemo API specs. OIH Connector </p>

## Description

A generated OIH connector for the Zistemo API specs. API (version 1.19.0).

Generated from: https://api.zistemo.com/{account}<br/>
Generated at: 2022-06-27T11:47:58+02:00

## API Description

Zistemo API<br/>

## Authorization

Supported authorization schemes:
- API Key

- API Key

- API Key

- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Internationalization
> The language function (?app_language) returns all messages of this action in a specific language.<br/>If ?app_language is not set than all retuning messages are in English. Each REST API request should include the language function like <code>https://api.zistemo.com/[tenant]/{action}?api_dev_key={key}&app_language=en</code> - [tenant] - your zistemo.com subdomain {action} - action like country, client, expense, login, vendor ...<br/>For example: when you ask for a list of countries use <code>https://api.zistemo.com/[tenant]/settings/countries?api_dev_key={key}</code> and you receive a list with all countries in English as default if you want them in German than add <code>?app_language=de</code>.<br/>For example: <code>https://api.zistemo.com/[tenant]/projects/billingmethods?api_dev_key={key}</code> returns the billing methods in English as default <code>https://api.zistemo.com/[tenant]/projects/billingmethods?api_dev_key={key}?app_language=de</code> returns the billing methods in German while <code>https://api.zistemo.com/[tenant]/projects/billingmethods?api_dev_key={key}?app_language=fr</code> returns the billing methods in France.<br/><br/>Available languages:<br/>* 'en' for English (default)<br/>* 'de' for Germany<br/>* 'es' for Spain<br/>* 'fr' for France<br/>* 'it' for Italy<br/>* 'pl' for Poland<br/>* 'cs' for Czech Republic<br/>* 'pt' for Portugal<br/>* 'ru' for Russia<br/>* 'ua' for Ukraine<br/>

*Tags:* `Introduction`

### Authentication
> You always need to add your private API Developer Key to have access to the API.<br/>Keep the API Developer Key private like as all other credentials.<br/>You find your API Developer Key on your [profile](https://moneypenny.me/knowledge-base/content/api-info/)<br/><br/><b>Token based Authentication</b><br/>To get access token: call <code>POST https://api.zistemo.com/[tenant]/login?api_dev_key={key}</code> with the params:<br/><code>email</code> - your email or username<br/><code>password</code> - your password<br/>Full call for CURL is:<br/><code>curl -d "email={email}&password={password}" -X POST https://api.zistemo.com/[tenant]/login?api_dev_key={key}</code> or <br/><code>curl -d "email={email}&password={password}" -H "api_dev_key:{key}" -X POST https://api.zistemo.com/[tenant]/login</code></br></br>The returned access token is valid for two hours. You need to use the returned access token for all API calls:<br/>* to the header parameter "Authorization" with the value of the access token, for example "Authorization = Bearer [access token]".<br/><code>curl -H "api_dev_key:{key}" -H "Authorization: Bearer {access token}"  -X GET https://api.zistemo.com/{account}/settings/countries</code><br/>* or as a URL parameter like:<br/><code>GET https://api.zistemo.com/{account}/settings/countries?token={access_token}?api_dev_key={key}</code><br/>Each REST API request should include the <code>api_dev_key</code> parameter https://api.zistemo.com/[tenant]/{action}?api_dev_key={key}, or the request header parameter <code>api_dev_key</code> with your api development key.<br/>

*Tags:* `Introduction`

### Create a new unit
> Creates new unit<br/>

*Tags:* `Units`

### Mark task as deleted
> Change task status into deleted<br/>

*Tags:* `Tasks`

#### Input Parameters
* `id` - _required_ - Identifier of requested task<br/>

### Update a task

*Tags:* `Tasks`

#### Input Parameters
* `id` - _required_ - Identifier of requested label<br/>

### Get a task
> Returns task details<br/>

*Tags:* `Tasks`

#### Input Parameters
* `id` - _required_ - Identifier of requested task<br/>

### Create an item
> Creates new item<br/>

*Tags:* `Items`

### Update an item
> Update item details<br/>

*Tags:* `Items`

#### Input Parameters
* `id` - _required_ - Identifier of requested item<br/>

### Mark item as archive
> Change item status into archived<br/>

*Tags:* `Items`

#### Input Parameters
* `id` - _required_ - Identifier of requested item<br/>

### Update an unit
> Update task<br/>

*Tags:* `Units`

#### Input Parameters
* `id` - _required_ - Identifier of requested unit<br/>

### Delete an unit

*Tags:* `Units`

#### Input Parameters
* `id` - _required_ - Identifier of requested unit<br/>

### Update a vendor
> Update vendor<br/>

*Tags:* `Vendors`

#### Input Parameters
* `id` - _required_ - Identifier of requested vendor<br/>

### Create a vendor
> Creates a vendor<br/>

*Tags:* `Vendors`

### Create a new Task
> Creates new task<br/>

*Tags:* `Tasks`

### Add/change vendor logo

*Tags:* `Vendors`

#### Input Parameters
* `id` - _required_ - Vendor ID<br/>

### Mark Vendor as active
> Mark vendor as active<br/>

*Tags:* `Vendors`

#### Input Parameters
* `id` - _required_ - Identifier of requested vendor<br/>

### Mark task as active
> Change task status into active<br/>

*Tags:* `Tasks`

#### Input Parameters
* `id` - _required_ - Identifier of requested task<br/>

### Delete Vendor logo
> Deletes vendor logo<br/>

*Tags:* `Vendors`

#### Input Parameters
* `id` - _required_ - Identifier of requested vendor<br/>

### Update a team

*Tags:* `Teams`

#### Input Parameters
* `id` - _required_ - Identifier of requested team<br/>

### Mark Vendor as deleted
> Mark vendor as deleted<br/>

*Tags:* `Vendors`

#### Input Parameters
* `id` - _required_ - Identifier of requested vendor<br/>

### Deactivate a team

*Tags:* `Teams`

#### Input Parameters
* `id` - _required_ - Identifier of requested team<br/>

### Get an item
> Returns item details<br/>

*Tags:* `Items`

#### Input Parameters
* `id` - _required_ - Identifier of requested item<br/>

### Mark item as active
> Change item status into active<br/>

*Tags:* `Items`

#### Input Parameters
* `id` - _required_ - Identifier of requested item<br/>

### Create a client
> Create client<br/>

*Tags:* `Clients`

### Activate a team

*Tags:* `Teams`

#### Input Parameters
* `id` - _required_ - Identifier of requested team<br/>

### Get a client
> Returns client details<br/>

*Tags:* `Clients`

#### Input Parameters
* `id` - _required_ - Identifier of requested client<br/>

### Mark item as deleted
> Change item status into deleted<br/>

*Tags:* `Items`

#### Input Parameters
* `id` - _required_ - Identifier of requested item<br/>

### Update a client
> Update client<br/>

*Tags:* `Clients`

#### Input Parameters
* `id` - _required_ - Identifier of requested client<br/>

### Add/change client logo

*Tags:* `Clients`

#### Input Parameters
* `id` - _required_ - Client ID<br/>

### Mark client as active

*Tags:* `Clients`

#### Input Parameters
* `id` - _required_ - Identifier of requested client<br/>

### Delete Client logo
> Deletes client logo<br/>

*Tags:* `Clients`

#### Input Parameters
* `id` - _required_ - Identifier of requested client<br/>

### Mark client as archived

*Tags:* `Clients`

#### Input Parameters
* `id` - _required_ - Identifier of requested client<br/>

### Get an invoice

*Tags:* `Invoices`

#### Input Parameters
* `id` - _required_ - Identifier of requested invoice<br/>

### Mark task as archive
> Change task status into archive<br/>

*Tags:* `Tasks`

#### Input Parameters
* `id` - _required_ - Identifier of requested task<br/>

### Create an invoice payment
> Creates new invoice payment<br/>

*Tags:* `Invoices`

#### Input Parameters
* `invoice_id` - _required_ - Identifier of requested invoice<br/>

### Update user details

*Tags:* `Users`

#### Input Parameters
* `id` - _required_ - User ID<br/>

### Get a unit
> Returns unit details<br/>

*Tags:* `Units`

#### Input Parameters
* `id` - _required_ - Identifier of requested unit<br/>

### Mark client as deleted

*Tags:* `Clients`

#### Input Parameters
* `id` - _required_ - Identifier of requested client<br/>

### Add/change user logo

*Tags:* `Users`

#### Input Parameters
* `id` - _required_ - User ID<br/>

### Create a user
> Creates user<br/>

*Tags:* `Users`

### Activate user

*Tags:* `Users`

#### Input Parameters
* `id` - _required_ - Identifier of requested user<br/>

### Delete Current User logo
> Deletes User logo<br/>

*Tags:* `Users`

### Deactivate a user

*Tags:* `Users`

#### Input Parameters
* `id` - _required_ - Identifier of requested user<br/>

### Get a user

*Tags:* `Users`

#### Input Parameters
* `id` - _required_ - Identifier of requested user<br/>

### Change user clock in / clock out status

*Tags:* `Users`

### Delete User logo
> Deletes User logo<br/>

*Tags:* `Users`

#### Input Parameters
* `id` - _required_ - Identifier of requested User<br/>

### Get a leave details

*Tags:* `Attendance`

#### Input Parameters
* `id` - _required_ - Identifier of requested leave<br/>

### Rate Limiting
> The limit is currently around 100 requests per 60 seconds per API access token, but this is not guaranteed: it may vary with server load, and we may change it in the future. You will receive a 429 HTTP response if you exceed the rate limit. Retry-After response header will specify the number of seconds after the user can make another request.Please contact us first, if you need perform a batch of API requests. Maybe we can provide you a more convenient way to retrieve the data.<br/>

*Tags:* `Introduction`

### Add/change current user logo

*Tags:* `Users`

### Create a user leave
> Create new user leave<br/>

*Tags:* `Attendance`

### Mark Vendor as archived
> Mark vendor as archived<br/>

*Tags:* `Vendors`

#### Input Parameters
* `id` - _required_ - Identifier of requested vendor<br/>

### Get currency

*Tags:* `Currency`

#### Input Parameters
* `id` - _required_ - Identifier of requested currency<br/>

### Get a team

*Tags:* `Teams`

#### Input Parameters
* `id` - _required_ - Identifier of requested team<br/>

### Delete a currency

*Tags:* `Currency`

#### Input Parameters
* `id` - _required_ - Identifier of requested currency<br/>

### Get an invoice payment

*Tags:* `Invoices`

#### Input Parameters
* `id` - _required_ - Identifier of requested invoice payment<br/>

### Update a user leave
> Update user leave details<br/>

*Tags:* `Attendance`

#### Input Parameters
* `id` - _required_ - Identifier of requested user leave<br/>

### Update a currency

*Tags:* `Currency`

#### Input Parameters
* `id` - _required_ - Id of currency<br/>

### Delete a user leave

*Tags:* `Attendance`

#### Input Parameters
* `id` - _required_ - Identifier of requested user leave<br/>

### Create a currency

*Tags:* `Currency`

### Get a project

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>
* `skip_time_entries` - _optional_ - do not load "time_sheets" list in response<br/>

### Update a project

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>

### Set a time ticket completed value

*Tags:* `Time tickets`

#### Input Parameters
* `id` - _required_ - Identifier of requested time ticket<br/>

### Get a time ticket details

*Tags:* `Time tickets`

#### Input Parameters
* `id` - _required_ - Identifier of requested time ticket<br/>

### Set a time ticket tentative value

*Tags:* `Time tickets`

#### Input Parameters
* `id` - _required_ - Identifier of requested time ticket<br/>

### Mark project as active

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>

### Update an invoice payment
> Updates invoice payment<br/>

*Tags:* `Invoices`

#### Input Parameters
* `id` - _required_ - Identifier of requested invoice payment<br/>

### Create a project

*Tags:* `Project`

### Open project, mark all tasks as active

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>

### Get an expense

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense ID<br/>

### Update an expense

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense ID<br/>

### Mark project as archived

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>

### Mark project as deleted

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>

### Create a category

*Tags:* `Expenses`

### Delete a category

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense category ID<br/>

### Delete an expense

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense ID<br/>

### Create an expense

*Tags:* `Expenses`

### Change user leave status

*Tags:* `Attendance`

#### Input Parameters
* `id` - _required_ - Identifier of requested user leave<br/>

### Delete a receipt

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense ID<br/>

### Create/Update exchange rate
> If rate for this date is not exist then it will be created. If rate for this date is exist then rate will be updated<br/>

*Tags:* `Currency`

#### Input Parameters
* `id` - _required_ - Identifier of requested currency<br/>

### Delete a sub-category

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense sub-category ID<br/>

### Create a sub-category

*Tags:* `Expenses`

### Mark expense as deleted
> Change expense status into deleted<br/>

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Identifier of requested expense<br/>

### Update a category

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - ID of category<br/>

### Close project, mark all tasks as done

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>

### Update an expense with multiple items

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - test<br/>

### Create an expense with multiple items

*Tags:* `Expenses`

### Start new timer

*Tags:* `Timer`

### Attach a receipt

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense ID<br/>

### Mark expense as active
> Change expense status into active<br/>

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Identifier of requested expense<br/>

### Get expense sub-categories

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Expense category ID<br/>
* `subId` - _required_ - Expense sub-category ID<br/>

### Update an mileage

*Tags:* `Mileages`

#### Input Parameters
* `id` - _required_ - ID of mileage<br/>

### Create an mileage

*Tags:* `Mileages`

### Mark mileage as archive
> Change mileage status into archive<br/>

*Tags:* `Mileages`

#### Input Parameters
* `id` - _required_ - Identifier of requested mileage<br/>

### Mark mileage as deleted
> Change mileage status into deleted<br/>

*Tags:* `Mileages`

#### Input Parameters
* `id` - _required_ - Identifier of requested mileage<br/>

### Uncompensate mileage
> Change mileage compensation status<br/>

*Tags:* `Mileages`

#### Input Parameters
* `id` - _required_ - Identifier of requested mileage<br/>

### Mark mileage as active
> Change mileage status into active<br/>

*Tags:* `Mileages`

#### Input Parameters
* `id` - _required_ - Identifier of requested mileage<br/>

### Cancel timer
> This request will remove all time gaps from timer and stop it without saving data<br/>

*Tags:* `Timer`

### Update timer

*Tags:* `Timer`

### Compensate mileage
> Change mileage compensation status<br/>

*Tags:* `Mileages`

#### Input Parameters
* `id` - _required_ - Identifier of requested mileage<br/>

### Submit for approval hours

*Tags:* `Time Tracking Approval`

#### Input Parameters
* `date` - _required_
* `user_id` - _required_ - Identifier of user<br/>

### Unlock approved week

*Tags:* `Time Tracking Approval`

#### Input Parameters
* `date` - _required_
* `user_id` - _required_ - Identifier of user<br/>

### Approve submitted for approval week

*Tags:* `Time Tracking Approval`

#### Input Parameters
* `date` - _required_
* `user_id` - _required_ - Identifier of user<br/>

### Add week note

*Tags:* `Time Tracking Approval`

#### Input Parameters
* `date` - _required_
* `user_id` - _required_ - Identifier of user<br/>
* `notes` - _required_ - Notes<br/>

### Create a time entry

*Tags:* `Timesheets`

### Delete a time entry

*Tags:* `Timesheets`

#### Input Parameters
* `id` - _required_ - Project ID<br/>

### Reset timer
> This request will remove all time gaps from timer object and restart timer<br/>

*Tags:* `Timer`

### Reject submitted for approval week

*Tags:* `Time Tracking Approval`

#### Input Parameters
* `date` - _required_
* `user_id` - _required_ - Identifier of user<br/>

### Mark expense as archive
> Change expense status into archive<br/>

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - Identifier of requested expense<br/>

### Update a sub-category

*Tags:* `Expenses`

#### Input Parameters
* `id` - _required_ - ID of sub-category<br/>

### Update a time entry

*Tags:* `Timesheets`

#### Input Parameters
* `id` - _required_ - TimeSheet entry id<br/>

### Update a company tax info

*Tags:* `Settings`

### Update company logo image

*Tags:* `Settings`

### Update a company bank info

*Tags:* `Settings`

### Delete company logo image

*Tags:* `Settings`

### Stop timer
> This request will stop current timer and add logged time to user timesheets<br/>

*Tags:* `Timer`

### Update a tax

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Tax ID<br/>

### Get a tax group

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Tax Group Id<br/>

### Get a tax

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Tax Id<br/>

### Update a tax group

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Tax group ID<br/>

### Delete a tax group

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Tax group ID<br/>

### Update company preferences

*Tags:* `Settings`

### Delete a tax

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Tax ID<br/>

### Create a team

*Tags:* `Teams`

### Update company profile

*Tags:* `Settings`

### Update a company address

*Tags:* `Settings`

### Create/Update stripe settings

*Tags:* `Settings`

### Update company template settings

*Tags:* `Settings`

### Create a term

*Tags:* `Settings`

### Activate/Disactivate stripe

*Tags:* `Settings`

#### Input Parameters
* `action` - _required_ - Activate/Deactivate<br/>
    Possible values: activate, disactivate.

### Create a tax group

*Tags:* `Settings`

### Create/Update paypal settings

*Tags:* `Settings`

### Create client/project custom field

*Tags:* `Settings`

#### Input Parameters
* `type` - _required_
    Possible values: client, project.

### Update client/project custom field

*Tags:* `Settings`

#### Input Parameters
* `type` - _required_
    Possible values: client, project.
* `id` - _required_ - Custom field ID<br/>

### Get a vendor
> Returns vendor details<br/>

*Tags:* `Vendors`

#### Input Parameters
* `id` - _required_ - Identifier of requested vendor<br/>

### Update number group

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Number group ID<br/>

### Get client/project custom field details

*Tags:* `Settings`

#### Input Parameters
* `type` - _required_
    Possible values: client, project.
* `id` - _required_ - Custom field ID<br/>

### Activate/Disactivate paypal

*Tags:* `Settings`

#### Input Parameters
* `action` - _required_ - Activate/Deactivate<br/>
    Possible values: activate, disactivate.

### Get formatted date

*Tags:* `Settings`

### Create a tax

*Tags:* `Settings`

### Delete client/project custom field

*Tags:* `Settings`

#### Input Parameters
* `type` - _required_
    Possible values: client, project.
* `id` - _required_ - Custom field ID<br/>

### Delete a term

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Identifier of requested term<br/>

### Pause timer

*Tags:* `Timer`

### Update project tasks assignment

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - ID of project<br/>

### Get client/project custom field list

*Tags:* `Settings`

#### Input Parameters
* `type` - _required_
    Possible values: client, project.

### Get number group details

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_ - Number group ID<br/>

### Update a term

*Tags:* `Settings`

#### Input Parameters
* `id` - _required_

## License

: zistemo<br/>
                    <br/>

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
