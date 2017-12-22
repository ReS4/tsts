# Getting started

Clicksend v3 API

## How to Build


You must have Python ```2 >=2.7.9``` or Python ```3 >=3.4``` installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=ClickSend-Python)


## How to Use

The following section explains how to use the ClickSend SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=ClickSend-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=ClickSend-Python&projectName=click_send)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=ClickSend-Python&projectName=click_send)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=ClickSend-Python&projectName=click_send)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from click_send.click_send import ClickSend
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=ClickSend-Python&libraryName=click_send.click_send&projectName=click_send&className=ClickSend)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=ClickSend-Python&libraryName=click_send.click_send&projectName=click_send&className=ClickSend)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke ```pip install -r test-requirements.txt```
  3. Invoke ```nosetests```

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| username | your username |
| key | your api key |



API client can be initialized as following.

```python
# Configuration parameters and credentials
username = 'username' # your username
key = 'key' # your api key

client = ClickSend(username, key)
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [CountriesController](#countries_controller)
* [SMSController](#sms_controller)
* [VoiceController](#voice_controller)
* [AccountController](#account_controller)
* [SubaccountController](#subaccount_controller)
* [ContactListController](#contact_list_controller)
* [ContactController](#contact_controller)
* [NumberController](#number_controller)
* [StatisticsController](#statistics_controller)
* [EmailToSmsController](#email_to_sms_controller)
* [SearchController](#search_controller)
* [ReferralAccountController](#referral_account_controller)
* [ResellerAccountController](#reseller_account_controller)
* [TransferCreditController](#transfer_credit_controller)
* [AccountRechargeController](#account_recharge_controller)
* [SmsCampaignController](#sms_campaign_controller)
* [PostLetterController](#post_letter_controller)
* [PostReturnAddressController](#post_return_address_controller)
* [FaxController](#fax_controller)
* [MMSController](#mms_controller)
* [PostPostcardController](#post_postcard_controller)
* [UploadController](#upload_controller)
* [PostDirectMailController](#post_direct_mail_controller)

## <a name="countries_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CountriesController") CountriesController

### Get controller instance

An instance of the ``` CountriesController ``` class can be accessed from the API Client.

```python
 countries_controller = client.countries
```

### <a name="get_countries"></a>![Method: ](https://apidocs.io/img/method.png ".CountriesController.get_countries") get_countries

> *Tags:*  ``` Skips Authentication ``` 

> Get all countries

```python
def get_countries(self)
```

#### Example Usage

```python

result = countries_controller.get_countries()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sms_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SMSController") SMSController

### Get controller instance

An instance of the ``` SMSController ``` class can be accessed from the API Client.

```python
 sms_controller = client.sms
```

### <a name="send_sms"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.send_sms") send_sms

> Send one or more SMS messages

```python
def send_sms(self,
                 sms_messages)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| smsMessages |  ``` Required ```  | SmsMessageCollection model |



#### Example Usage

```python
sms_messages = SmsMessageCollection()

result = sms_controller.send_sms(sms_messages)

```


### <a name="calculate_price"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.calculate_price") calculate_price

> Calculate sms price

```python
def calculate_price(self,
                        sms_messages)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| smsMessages |  ``` Required ```  | SmsMessageCollection model |



#### Example Usage

```python
sms_messages = SmsMessageCollection()

result = sms_controller.calculate_price(sms_messages)

```


### <a name="export_history"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.export_history") export_history

> Export all sms history

```python
def export_history(self,
                       filename)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filename |  ``` Required ```  | Filename to download history as |



#### Example Usage

```python
filename = 'filename'

result = sms_controller.export_history(filename)

```


### <a name="create_receipt"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.create_receipt") create_receipt

> Add a delivery receipt

```python
def create_receipt(self,
                       url)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| url |  ``` Required ```  | Your url |



#### Example Usage

```python
url = 'url'

result = sms_controller.create_receipt(url)

```


### <a name="mark_receipts_as_read"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.mark_receipts_as_read") mark_receipts_as_read

> Marked delivery receipts as read

```python
def mark_receipts_as_read(self,
                              date_before=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| dateBefore |  ``` Optional ```  | Mark all as read before this timestamp |



#### Example Usage

```python
date_before = 'date_before'

result = sms_controller.mark_receipts_as_read(date_before)

```


### <a name="get_inbound_sms"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.get_inbound_sms") get_inbound_sms

> Get all inbound sms

```python
def get_inbound_sms(self)
```

#### Example Usage

```python

result = sms_controller.get_inbound_sms()

```


### <a name="create_inbound_sms"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.create_inbound_sms") create_inbound_sms

> Create inbound sms

```python
def create_inbound_sms(self,
                           url)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| url |  ``` Required ```  | Your url |



#### Example Usage

```python
url = 'url'

result = sms_controller.create_inbound_sms(url)

```


### <a name="cancel_scheduled_sms"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.cancel_scheduled_sms") cancel_scheduled_sms

> Update scheduled message as cancel

```python
def cancel_scheduled_sms(self,
                             message_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageId |  ``` Required ```  | The message ID you want to cancel |



#### Example Usage

```python
message_id = 'message_id'

result = sms_controller.cancel_scheduled_sms(message_id)

```


### <a name="cancel_all_scheduled_sms"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.cancel_all_scheduled_sms") cancel_all_scheduled_sms

> Update all scheduled message as cancelled

```python
def cancel_all_scheduled_sms(self)
```

#### Example Usage

```python

result = sms_controller.cancel_all_scheduled_sms()

```


### <a name="create_sms_template"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.create_sms_template") create_sms_template

> Create sms template

```python
def create_sms_template(self,
                            sms_template)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| smsTemplate |  ``` Required ```  | SmsTemplate model |



#### Example Usage

```python
sms_template = SmsTemplate()

result = sms_controller.create_sms_template(sms_template)

```


### <a name="delete_sms_template"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.delete_sms_template") delete_sms_template

> Delete sms template

```python
def delete_sms_template(self,
                            template_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| templateId |  ``` Required ```  | Template id |



#### Example Usage

```python
template_id = 105

result = sms_controller.delete_sms_template(template_id)

```


### <a name="update_sms_template"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.update_sms_template") update_sms_template

> Update sms template

```python
def update_sms_template(self,
                            template_id,
                            sms_template)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| templateId |  ``` Required ```  | Template id |
| smsTemplate |  ``` Required ```  | Template item |



#### Example Usage

```python
template_id = 105
sms_template = SmsTemplate()

result = sms_controller.update_sms_template(template_id, sms_template)

```


### <a name="get_delivery_receipts"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.get_delivery_receipts") get_delivery_receipts

> Get all delivery receipts

```python
def get_delivery_receipts(self)
```

#### Example Usage

```python

result = sms_controller.get_delivery_receipts()

```


### <a name="get_sms_templates"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.get_sms_templates") get_sms_templates

> Get lists of all sms templates

```python
def get_sms_templates(self)
```

#### Example Usage

```python

result = sms_controller.get_sms_templates()

```


### <a name="mark_all_inbound_sms_as_read"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.mark_all_inbound_sms_as_read") mark_all_inbound_sms_as_read

> Mark all inbound SMS as read optionally before a certain date

```python
def mark_all_inbound_sms_as_read(self,
                                     date_before=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| dateBefore |  ``` Optional ```  | An optional timestamp - mark all as read before this timestamp. If not given, all messages will be marked as read. |



#### Example Usage

```python
date_before = 'date_before'

result = sms_controller.mark_all_inbound_sms_as_read(date_before)

```


### <a name="get_specific_delivery_receipt"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.get_specific_delivery_receipt") get_specific_delivery_receipt

> Get a Specific Delivery Receipt

```python
def get_specific_delivery_receipt(self,
                                      message_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageId |  ``` Required ```  | Message ID |



#### Example Usage

```python
message_id = 'message_id'

result = sms_controller.get_specific_delivery_receipt(message_id)

```


### <a name="get_sms_history"></a>![Method: ](https://apidocs.io/img/method.png ".SMSController.get_sms_history") get_sms_history

> Get all sms history

```python
def get_sms_history(self,
                        date_from=None,
                        date_to=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| dateFrom |  ``` Optional ```  | Start date |
| dateTo |  ``` Optional ```  | End date |



#### Example Usage

```python
date_from = 105
date_to = 105

result = sms_controller.get_sms_history(date_from, date_to)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="voice_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VoiceController") VoiceController

### Get controller instance

An instance of the ``` VoiceController ``` class can be accessed from the API Client.

```python
 voice_controller = client.voice
```

### <a name="send_voice"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.send_voice") send_voice

> Send a voice call

```python
def send_voice(self,
                   voice_messages)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| voiceMessages |  ``` Required ```  | VoiceMessageCollection model |



#### Example Usage

```python
voice_messages = VoiceMessageCollection()

result = voice_controller.send_voice(voice_messages)

```


### <a name="calculate_price"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.calculate_price") calculate_price

> Calculate voice price

```python
def calculate_price(self,
                        voice_messages)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| voiceMessages |  ``` Required ```  | VoiceMessageCollection model |



#### Example Usage

```python
voice_messages = VoiceMessageCollection()

result = voice_controller.calculate_price(voice_messages)

```


### <a name="get_voice_languages"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.get_voice_languages") get_voice_languages

> Get all voice languages

```python
def get_voice_languages(self)
```

#### Example Usage

```python

result = voice_controller.get_voice_languages()

```


### <a name="get_voice_receipts"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.get_voice_receipts") get_voice_receipts

> Get all voice receipts

```python
def get_voice_receipts(self)
```

#### Example Usage

```python

result = voice_controller.get_voice_receipts()

```


### <a name="cancel_voice_message"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.cancel_voice_message") cancel_voice_message

> Update voice message status as cancelled

```python
def cancel_voice_message(self,
                             message_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageId |  ``` Required ```  | Your voice message id |



#### Example Usage

```python
message_id = 'message_id'

result = voice_controller.cancel_voice_message(message_id)

```


### <a name="cancel_voice_messages"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.cancel_voice_messages") cancel_voice_messages

> Update all voice messages as cancelled

```python
def cancel_voice_messages(self)
```

#### Example Usage

```python

result = voice_controller.cancel_voice_messages()

```


### <a name="export_voice_history"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.export_voice_history") export_voice_history

> Export voice history

```python
def export_voice_history(self,
                             filename)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filename |  ``` Required ```  | Filename to export to |



#### Example Usage

```python
filename = 'filename'

result = voice_controller.export_voice_history(filename)

```


### <a name="get_voice_history"></a>![Method: ](https://apidocs.io/img/method.png ".VoiceController.get_voice_history") get_voice_history

> Get all voice history

```python
def get_voice_history(self,
                          date_from=None,
                          date_to=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| dateFrom |  ``` Optional ```  | Timestamp (from) used to show records by date. |
| dateTo |  ``` Optional ```  | Timestamp (to) used to show records by date |



#### Example Usage

```python
date_from = 196
date_to = 196

result = voice_controller.get_voice_history(date_from, date_to)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="account_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AccountController") AccountController

### Get controller instance

An instance of the ``` AccountController ``` class can be accessed from the API Client.

```python
 account_controller = client.account
```

### <a name="get_account"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.get_account") get_account

> Get account details

```python
def get_account(self)
```

#### Example Usage

```python

result = account_controller.get_account()

```


### <a name="create_account"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.create_account") create_account

> Create An Account

```python
def create_account(self,
                       account)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| account |  ``` Required ```  | Account model |



#### Example Usage

```python
account = Account()

result = account_controller.create_account(account)

```


### <a name="account_verify_send"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.account_verify_send") account_verify_send

> Send account activation token

```python
def account_verify_send(self,
                            account_verify)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accountVerify |  ``` Required ```  | Account details |



#### Example Usage

```python
account_verify = AccountVerify()

result = account_controller.account_verify_send(account_verify)

```


### <a name="account_verify"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.account_verify") account_verify

> Verify new account

```python
def account_verify(self,
                       activation_token)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| activationToken |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
activation_token = 196

result = account_controller.account_verify(activation_token)

```


### <a name="forgot_username"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.forgot_username") forgot_username

> *Tags:*  ``` Skips Authentication ``` 

> Forgot username

```python
def forgot_username(self,
                        email)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| email |  ``` Required ```  | Email belonging to account |



#### Example Usage

```python
email = 'email'

result = account_controller.forgot_username(email)

```


### <a name="forgot_password"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.forgot_password") forgot_password

> Forgot password

```python
def forgot_password(self,
                        username)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| username |  ``` Required ```  | Username belonging to account |



#### Example Usage

```python
username = 'username'

result = account_controller.forgot_password(username)

```


### <a name="verify_forgot_password"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.verify_forgot_password") verify_forgot_password

> Verify forgot password

```python
def verify_forgot_password(self,
                               verify_password)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| verifyPassword |  ``` Required ```  | verifyPassword data |



#### Example Usage

```python
verify_password = AccountForgotPasswordVerify()

result = account_controller.verify_forgot_password(verify_password)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="subaccount_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SubaccountController") SubaccountController

### Get controller instance

An instance of the ``` SubaccountController ``` class can be accessed from the API Client.

```python
 subaccount_controller = client.subaccount
```

### <a name="get_subaccounts"></a>![Method: ](https://apidocs.io/img/method.png ".SubaccountController.get_subaccounts") get_subaccounts

> Get all subaccounts

```python
def get_subaccounts(self)
```

#### Example Usage

```python

result = subaccount_controller.get_subaccounts()

```


### <a name="create_subaccount"></a>![Method: ](https://apidocs.io/img/method.png ".SubaccountController.create_subaccount") create_subaccount

> Create new subaccount

```python
def create_subaccount(self,
                          subaccount)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| subaccount |  ``` Required ```  | Subaccount model |



#### Example Usage

```python
subaccount = Subaccount()

result = subaccount_controller.create_subaccount(subaccount)

```


### <a name="get_subaccount"></a>![Method: ](https://apidocs.io/img/method.png ".SubaccountController.get_subaccount") get_subaccount

> Get specific subaccount

```python
def get_subaccount(self,
                       subaccount_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| subaccountId |  ``` Required ```  | ID of subaccount to get |



#### Example Usage

```python
subaccount_id = 196

result = subaccount_controller.get_subaccount(subaccount_id)

```


### <a name="delete_subaccount"></a>![Method: ](https://apidocs.io/img/method.png ".SubaccountController.delete_subaccount") delete_subaccount

> Delete a subaccount

```python
def delete_subaccount(self,
                          subaccount_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| subaccountId |  ``` Required ```  | ID of subaccount to delete |



#### Example Usage

```python
subaccount_id = 196

result = subaccount_controller.delete_subaccount(subaccount_id)

```


### <a name="regenerate_api_key"></a>![Method: ](https://apidocs.io/img/method.png ".SubaccountController.regenerate_api_key") regenerate_api_key

> Regenerate an API Key

```python
def regenerate_api_key(self,
                           subaccount_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| subaccountId |  ``` Required ```  | ID of subaccount to regenerate API key for |



#### Example Usage

```python
subaccount_id = 196

result = subaccount_controller.regenerate_api_key(subaccount_id)

```


### <a name="update_subaccount"></a>![Method: ](https://apidocs.io/img/method.png ".SubaccountController.update_subaccount") update_subaccount

> Update subaccount

```python
def update_subaccount(self,
                          subaccount_id,
                          subaccount)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| subaccountId |  ``` Required ```  | ID of subaccount to update |
| subaccount |  ``` Required ```  | Subaccount model |



#### Example Usage

```python
subaccount_id = 196
subaccount = Subaccount()

result = subaccount_controller.update_subaccount(subaccount_id, subaccount)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="contact_list_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ContactListController") ContactListController

### Get controller instance

An instance of the ``` ContactListController ``` class can be accessed from the API Client.

```python
 contact_list_controller = client.contact_list
```

### <a name="get_contact_lists"></a>![Method: ](https://apidocs.io/img/method.png ".ContactListController.get_contact_lists") get_contact_lists

> Get all contact lists

```python
def get_contact_lists(self)
```

#### Example Usage

```python

result = contact_list_controller.get_contact_lists()

```


### <a name="create_contact_list"></a>![Method: ](https://apidocs.io/img/method.png ".ContactListController.create_contact_list") create_contact_list

> Create new contact list

```python
def create_contact_list(self,
                            list_name)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listName |  ``` Required ```  | Your contact list name |



#### Example Usage

```python
list_name = 'list_name'

result = contact_list_controller.create_contact_list(list_name)

```


### <a name="get_contact_list"></a>![Method: ](https://apidocs.io/img/method.png ".ContactListController.get_contact_list") get_contact_list

> Get specific contact list

```python
def get_contact_list(self,
                         list_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | List ID |



#### Example Usage

```python
list_id = 196

result = contact_list_controller.get_contact_list(list_id)

```


### <a name="delete_contact_list"></a>![Method: ](https://apidocs.io/img/method.png ".ContactListController.delete_contact_list") delete_contact_list

> Delete a specific contact list

```python
def delete_contact_list(self,
                            list_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | List ID |



#### Example Usage

```python
list_id = 196

result = contact_list_controller.delete_contact_list(list_id)

```


### <a name="remove_duplicate_contacts"></a>![Method: ](https://apidocs.io/img/method.png ".ContactListController.remove_duplicate_contacts") remove_duplicate_contacts

> Remove duplicate contacts

```python
def remove_duplicate_contacts(self,
                                  list_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | Your list id |



#### Example Usage

```python
list_id = 196

result = contact_list_controller.remove_duplicate_contacts(list_id)

```


### <a name="update_contact_list"></a>![Method: ](https://apidocs.io/img/method.png ".ContactListController.update_contact_list") update_contact_list

> Update specific contact list

```python
def update_contact_list(self,
                            list_id,
                            list_name)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | Your list id |
| listName |  ``` Required ```  | Your new list name |



#### Example Usage

```python
list_id = 196
list_name = 'list_name'

result = contact_list_controller.update_contact_list(list_id, list_name)

```


### <a name="import_contacts_to_list"></a>![Method: ](https://apidocs.io/img/method.png ".ContactListController.import_contacts_to_list") import_contacts_to_list

> Import contacts to list

```python
def import_contacts_to_list(self,
                                list_id,
                                file)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | Your contact list id you want to access. |
| file |  ``` Required ```  | ContactListImport model |



#### Example Usage

```python
list_id = 196
file = ContactListImport()

result = contact_list_controller.import_contacts_to_list(list_id, file)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="contact_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ContactController") ContactController

### Get controller instance

An instance of the ``` ContactController ``` class can be accessed from the API Client.

```python
 contact_controller = client.contact
```

### <a name="get_contacts"></a>![Method: ](https://apidocs.io/img/method.png ".ContactController.get_contacts") get_contacts

> Get all contacts in a list

```python
def get_contacts(self,
                     list_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | Contact list ID |



#### Example Usage

```python
list_id = 196

result = contact_controller.get_contacts(list_id)

```


### <a name="create_contact"></a>![Method: ](https://apidocs.io/img/method.png ".ContactController.create_contact") create_contact

> Create new contact

```python
def create_contact(self,
                       contact,
                       list_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contact |  ``` Required ```  | Contact model |
| listId |  ``` Required ```  | List id |



#### Example Usage

```python
contact = Contact()
list_id = 196

result = contact_controller.create_contact(contact, list_id)

```


### <a name="get_contact"></a>![Method: ](https://apidocs.io/img/method.png ".ContactController.get_contact") get_contact

> Get a specific contact

```python
def get_contact(self,
                    list_id,
                    contact_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | Your contact list id you want to access. |
| contactId |  ``` Required ```  | Your contact id you want to access. |



#### Example Usage

```python
list_id = 196
contact_id = 196

result = contact_controller.get_contact(list_id, contact_id)

```


### <a name="update_contact"></a>![Method: ](https://apidocs.io/img/method.png ".ContactController.update_contact") update_contact

> Update contact

```python
def update_contact(self,
                       list_id,
                       contact_id,
                       contact)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | Contact list id |
| contactId |  ``` Required ```  | Contact ID |
| contact |  ``` Required ```  | Contact model |



#### Example Usage

```python
list_id = 196
contact_id = 196
contact = Contact()

result = contact_controller.update_contact(list_id, contact_id, contact)

```


### <a name="remove_opted_out_contacts"></a>![Method: ](https://apidocs.io/img/method.png ".ContactController.remove_opted_out_contacts") remove_opted_out_contacts

> Remove all opted out contacts

```python
def remove_opted_out_contacts(self,
                                  list_id,
                                  opt_out_list_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | Your list id |
| optOutListId |  ``` Required ```  | Your opt out list id |



#### Example Usage

```python
list_id = 196
opt_out_list_id = 196

result = contact_controller.remove_opted_out_contacts(list_id, opt_out_list_id)

```


### <a name="delete_contact"></a>![Method: ](https://apidocs.io/img/method.png ".ContactController.delete_contact") delete_contact

> Delete a contact

```python
def delete_contact(self,
                       list_id,
                       contact_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| listId |  ``` Required ```  | List ID |
| contactId |  ``` Required ```  | Contact ID |



#### Example Usage

```python
list_id = 196
contact_id = 196

result = contact_controller.delete_contact(list_id, contact_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="number_controller"></a>![Class: ](https://apidocs.io/img/class.png ".NumberController") NumberController

### Get controller instance

An instance of the ``` NumberController ``` class can be accessed from the API Client.

```python
 number_controller = client.number
```

### <a name="get_dedicated_numbers"></a>![Method: ](https://apidocs.io/img/method.png ".NumberController.get_dedicated_numbers") get_dedicated_numbers

> Get all dedicated numbers

```python
def get_dedicated_numbers(self)
```

#### Example Usage

```python

result = number_controller.get_dedicated_numbers()

```


### <a name="purchase_dedicated_number"></a>![Method: ](https://apidocs.io/img/method.png ".NumberController.purchase_dedicated_number") purchase_dedicated_number

> Buy dedicated number

```python
def purchase_dedicated_number(self,
                                  dedicated_number)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| dedicatedNumber |  ``` Required ```  | Phone number to purchase |



#### Example Usage

```python
dedicated_number = 'dedicated_number'

result = number_controller.purchase_dedicated_number(dedicated_number)

```


### <a name="get_dedicated_numbers_by_country"></a>![Method: ](https://apidocs.io/img/method.png ".NumberController.get_dedicated_numbers_by_country") get_dedicated_numbers_by_country

> Get all dedicated numbers by country

```python
def get_dedicated_numbers_by_country(self,
                                         country,
                                         search=None,
                                         search_type=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| country |  ``` Required ```  | Country code to search |
| search |  ``` Optional ```  | Your search pattern or query. |
| searchType |  ``` Optional ```  | Your strategy for searching, 0 = starts with, 1 = anywhere, 2 = ends with. |



#### Example Usage

```python
country = 'country'
search = 'search'
search_type = 196

result = number_controller.get_dedicated_numbers_by_country(country, search, search_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="statistics_controller"></a>![Class: ](https://apidocs.io/img/class.png ".StatisticsController") StatisticsController

### Get controller instance

An instance of the ``` StatisticsController ``` class can be accessed from the API Client.

```python
 statistics_controller = client.statistics
```

### <a name="get_voice_statistics"></a>![Method: ](https://apidocs.io/img/method.png ".StatisticsController.get_voice_statistics") get_voice_statistics

> Get voice statistics

```python
def get_voice_statistics(self)
```

#### Example Usage

```python

result = statistics_controller.get_voice_statistics()

```


### <a name="get_sms_statistics"></a>![Method: ](https://apidocs.io/img/method.png ".StatisticsController.get_sms_statistics") get_sms_statistics

> Get sms statistics

```python
def get_sms_statistics(self)
```

#### Example Usage

```python

result = statistics_controller.get_sms_statistics()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="email_to_sms_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EmailToSmsController") EmailToSmsController

### Get controller instance

An instance of the ``` EmailToSmsController ``` class can be accessed from the API Client.

```python
 email_to_sms_controller = client.email_to_sms
```

### <a name="create_allowed_address"></a>![Method: ](https://apidocs.io/img/method.png ".EmailToSmsController.create_allowed_address") create_allowed_address

> Create email to sms allowed address

```python
def create_allowed_address(self,
                               email_sms_address)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| emailSmsAddress |  ``` Required ```  | EmailSMSAddress model |



#### Example Usage

```python
email_sms_address = EmailSMSAddress()

result = email_to_sms_controller.create_allowed_address(email_sms_address)

```


### <a name="get_allowed_address"></a>![Method: ](https://apidocs.io/img/method.png ".EmailToSmsController.get_allowed_address") get_allowed_address

> Get list of email to sms allowed addresses

```python
def get_allowed_address(self)
```

#### Example Usage

```python

result = email_to_sms_controller.get_allowed_address()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="search_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SearchController") SearchController

### Get controller instance

An instance of the ``` SearchController ``` class can be accessed from the API Client.

```python
 search_controller = client.search
```

### <a name="search_contact_list"></a>![Method: ](https://apidocs.io/img/method.png ".SearchController.search_contact_list") search_contact_list

> Get list of searched contact list

```python
def search_contact_list(self,
                            q)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Required ```  | Your keyword or query. |



#### Example Usage

```python
q = 'q'

result = search_controller.search_contact_list(q)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="referral_account_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ReferralAccountController") ReferralAccountController

### Get controller instance

An instance of the ``` ReferralAccountController ``` class can be accessed from the API Client.

```python
 referral_account_controller = client.referral_account
```

### <a name="get_referral_accounts"></a>![Method: ](https://apidocs.io/img/method.png ".ReferralAccountController.get_referral_accounts") get_referral_accounts

> Get all referral accounts

```python
def get_referral_accounts(self)
```

#### Example Usage

```python

result = referral_account_controller.get_referral_accounts()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="reseller_account_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ResellerAccountController") ResellerAccountController

### Get controller instance

An instance of the ``` ResellerAccountController ``` class can be accessed from the API Client.

```python
 reseller_account_controller = client.reseller_account
```

### <a name="get_reseller_accounts"></a>![Method: ](https://apidocs.io/img/method.png ".ResellerAccountController.get_reseller_accounts") get_reseller_accounts

> Get list of reseller accounts

```python
def get_reseller_accounts(self)
```

#### Example Usage

```python

result = reseller_account_controller.get_reseller_accounts()

```


### <a name="create_reseller_account"></a>![Method: ](https://apidocs.io/img/method.png ".ResellerAccountController.create_reseller_account") create_reseller_account

> Create reseller account

```python
def create_reseller_account(self,
                                reseller_account)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| resellerAccount |  ``` Required ```  | ResellerAccount model |



#### Example Usage

```python
reseller_account = ResellerAccount()

result = reseller_account_controller.create_reseller_account(reseller_account)

```


### <a name="get_reseller_account"></a>![Method: ](https://apidocs.io/img/method.png ".ResellerAccountController.get_reseller_account") get_reseller_account

> Get Reseller Account

```python
def get_reseller_account(self,
                             client_user_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| clientUserId |  ``` Required ```  | User ID of client |



#### Example Usage

```python
client_user_id = 196

result = reseller_account_controller.get_reseller_account(client_user_id)

```


### <a name="update_reseller_account"></a>![Method: ](https://apidocs.io/img/method.png ".ResellerAccountController.update_reseller_account") update_reseller_account

> Reseller Account

```python
def update_reseller_account(self,
                                client_user_id,
                                reseller_account)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| clientUserId |  ``` Required ```  | User ID of client |
| resellerAccount |  ``` Required ```  | ResellerAccount model |



#### Example Usage

```python
client_user_id = 155
reseller_account = ResellerAccount()

result = reseller_account_controller.update_reseller_account(client_user_id, reseller_account)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="transfer_credit_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TransferCreditController") TransferCreditController

### Get controller instance

An instance of the ``` TransferCreditController ``` class can be accessed from the API Client.

```python
 transfer_credit_controller = client.transfer_credit
```

### <a name="transfer_credit"></a>![Method: ](https://apidocs.io/img/method.png ".TransferCreditController.transfer_credit") transfer_credit

> Transfer Credit

```python
def transfer_credit(self,
                        reseller_account_transfer_credit)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| resellerAccountTransferCredit |  ``` Required ```  | ResellerAccountTransferCredit model |



#### Example Usage

```python
reseller_account_transfer_credit = ResellerAccountTransferCredit()

result = transfer_credit_controller.transfer_credit(reseller_account_transfer_credit)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="account_recharge_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AccountRechargeController") AccountRechargeController

### Get controller instance

An instance of the ``` AccountRechargeController ``` class can be accessed from the API Client.

```python
 account_recharge_controller = client.account_recharge
```

### <a name="get_credit_card_info"></a>![Method: ](https://apidocs.io/img/method.png ".AccountRechargeController.get_credit_card_info") get_credit_card_info

> Get Credit Card info

```python
def get_credit_card_info(self)
```

#### Example Usage

```python

result = account_recharge_controller.get_credit_card_info()

```


### <a name="update_credit_card_info"></a>![Method: ](https://apidocs.io/img/method.png ".AccountRechargeController.update_credit_card_info") update_credit_card_info

> Update credit card info

```python
def update_credit_card_info(self,
                                credit_card)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| creditCard |  ``` Required ```  | CreditCard model |



#### Example Usage

```python
credit_card = CreditCard()

result = account_recharge_controller.update_credit_card_info(credit_card)

```


### <a name="get_packages_list"></a>![Method: ](https://apidocs.io/img/method.png ".AccountRechargeController.get_packages_list") get_packages_list

> Get list of all packages

```python
def get_packages_list(self,
                          country=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| country |  ``` Optional ```  | Country code |



#### Example Usage

```python
country = 'country'

result = account_recharge_controller.get_packages_list(country)

```


### <a name="purchase_package"></a>![Method: ](https://apidocs.io/img/method.png ".AccountRechargeController.purchase_package") purchase_package

> Purchase a package

```python
def purchase_package(self,
                         package_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| packageId |  ``` Required ```  | ID of package to purchase |



#### Example Usage

```python
package_id = 155

result = account_recharge_controller.purchase_package(package_id)

```


### <a name="get_transactions"></a>![Method: ](https://apidocs.io/img/method.png ".AccountRechargeController.get_transactions") get_transactions

> Get all transactions

```python
def get_transactions(self)
```

#### Example Usage

```python

result = account_recharge_controller.get_transactions()

```


### <a name="get_transaction"></a>![Method: ](https://apidocs.io/img/method.png ".AccountRechargeController.get_transaction") get_transaction

> Get specific Transaction

```python
def get_transaction(self,
                        transaction_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| transactionId |  ``` Required ```  | ID of transaction to retrieve |



#### Example Usage

```python
transaction_id = 'transaction_id'

result = account_recharge_controller.get_transaction(transaction_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sms_campaign_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SmsCampaignController") SmsCampaignController

### Get controller instance

An instance of the ``` SmsCampaignController ``` class can be accessed from the API Client.

```python
 sms_campaign_controller = client.sms_campaign
```

### <a name="create_sms_campaign"></a>![Method: ](https://apidocs.io/img/method.png ".SmsCampaignController.create_sms_campaign") create_sms_campaign

> Create sms campaign

```python
def create_sms_campaign(self,
                            campaign)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| campaign |  ``` Required ```  | SmsCampaign model |



#### Example Usage

```python
campaign = SmsCampaign()

result = sms_campaign_controller.create_sms_campaign(campaign)

```


### <a name="calculate_price"></a>![Method: ](https://apidocs.io/img/method.png ".SmsCampaignController.calculate_price") calculate_price

> Calculate price for sms campaign

```python
def calculate_price(self,
                        campaign)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| campaign |  ``` Required ```  | SmsCampaign model |



#### Example Usage

```python
campaign = SmsCampaign()

result = sms_campaign_controller.calculate_price(campaign)

```


### <a name="update_sms_campaign"></a>![Method: ](https://apidocs.io/img/method.png ".SmsCampaignController.update_sms_campaign") update_sms_campaign

> Update sms campaign

```python
def update_sms_campaign(self,
                            sms_campaign_id,
                            campaign)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| smsCampaignId |  ``` Required ```  | ID of SMS campaign to update |
| campaign |  ``` Required ```  | SmsCampaign model |



#### Example Usage

```python
sms_campaign_id = 155
campaign = SmsCampaign()

result = sms_campaign_controller.update_sms_campaign(sms_campaign_id, campaign)

```


### <a name="cancel_sms_campaign"></a>![Method: ](https://apidocs.io/img/method.png ".SmsCampaignController.cancel_sms_campaign") cancel_sms_campaign

> Cancel sms campaign

```python
def cancel_sms_campaign(self,
                            sms_campaign_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| smsCampaignId |  ``` Required ```  | ID of SMS Campaign to cancel |



#### Example Usage

```python
sms_campaign_id = 155

result = sms_campaign_controller.cancel_sms_campaign(sms_campaign_id)

```


### <a name="get_sms_campaigns"></a>![Method: ](https://apidocs.io/img/method.png ".SmsCampaignController.get_sms_campaigns") get_sms_campaigns

> Get list of sms campaigns

```python
def get_sms_campaigns(self)
```

#### Example Usage

```python

result = sms_campaign_controller.get_sms_campaigns()

```


### <a name="get_sms_campaign"></a>![Method: ](https://apidocs.io/img/method.png ".SmsCampaignController.get_sms_campaign") get_sms_campaign

> Get specific sms campaign

```python
def get_sms_campaign(self,
                         sms_campaign_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| smsCampaignId |  ``` Required ```  | ID of SMS campaign to retrieve |



#### Example Usage

```python
sms_campaign_id = 155

result = sms_campaign_controller.get_sms_campaign(sms_campaign_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="post_letter_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PostLetterController") PostLetterController

### Get controller instance

An instance of the ``` PostLetterController ``` class can be accessed from the API Client.

```python
 post_letter_controller = client.post_letter
```

### <a name="send_post_letter"></a>![Method: ](https://apidocs.io/img/method.png ".PostLetterController.send_post_letter") send_post_letter

> Send post letter

```python
def send_post_letter(self,
                         post_letter)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| postLetter |  ``` Required ```  | PostLetter model |



#### Example Usage

```python
post_letter = PostLetter()

result = post_letter_controller.send_post_letter(post_letter)

```


### <a name="calculate_price"></a>![Method: ](https://apidocs.io/img/method.png ".PostLetterController.calculate_price") calculate_price

> Calculate post letter price

```python
def calculate_price(self,
                        post_letter)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| postLetter |  ``` Required ```  | PostLetter model |



#### Example Usage

```python
post_letter = PostLetter()

result = post_letter_controller.calculate_price(post_letter)

```


### <a name="get_post_letter_history"></a>![Method: ](https://apidocs.io/img/method.png ".PostLetterController.get_post_letter_history") get_post_letter_history

> Get all post letter history

```python
def get_post_letter_history(self)
```

#### Example Usage

```python

result = post_letter_controller.get_post_letter_history()

```


### <a name="export_post_letter_history"></a>![Method: ](https://apidocs.io/img/method.png ".PostLetterController.export_post_letter_history") export_post_letter_history

> export post letter history

```python
def export_post_letter_history(self,
                                   filename)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filename |  ``` Required ```  | Filename to export to |



#### Example Usage

```python
filename = 'filename'

result = post_letter_controller.export_post_letter_history(filename)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="post_return_address_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PostReturnAddressController") PostReturnAddressController

### Get controller instance

An instance of the ``` PostReturnAddressController ``` class can be accessed from the API Client.

```python
 post_return_address_controller = client.post_return_address
```

### <a name="create_post_return_address"></a>![Method: ](https://apidocs.io/img/method.png ".PostReturnAddressController.create_post_return_address") create_post_return_address

> Create post return address

```python
def create_post_return_address(self,
                                   return_address)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| returnAddress |  ``` Required ```  | Address model |



#### Example Usage

```python
return_address = Address()

result = post_return_address_controller.create_post_return_address(return_address)

```


### <a name="get_post_return_addresses"></a>![Method: ](https://apidocs.io/img/method.png ".PostReturnAddressController.get_post_return_addresses") get_post_return_addresses

> Get list of post return addresses

```python
def get_post_return_addresses(self)
```

#### Example Usage

```python

result = post_return_address_controller.get_post_return_addresses()

```


### <a name="get_post_return_address"></a>![Method: ](https://apidocs.io/img/method.png ".PostReturnAddressController.get_post_return_address") get_post_return_address

> Get specific post return address

```python
def get_post_return_address(self,
                                return_address_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| returnAddressId |  ``` Required ```  | Return address ID |



#### Example Usage

```python
return_address_id = 155

result = post_return_address_controller.get_post_return_address(return_address_id)

```


### <a name="update_post_return_address"></a>![Method: ](https://apidocs.io/img/method.png ".PostReturnAddressController.update_post_return_address") update_post_return_address

> Update post return address

```python
def update_post_return_address(self,
                                   return_address_id,
                                   return_address)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| returnAddressId |  ``` Required ```  | Return address ID |
| returnAddress |  ``` Required ```  | Address model |



#### Example Usage

```python
return_address_id = 155
return_address = Address()

result = post_return_address_controller.update_post_return_address(return_address_id, return_address)

```


### <a name="delete_post_return_address"></a>![Method: ](https://apidocs.io/img/method.png ".PostReturnAddressController.delete_post_return_address") delete_post_return_address

> Delete specific post return address

```python
def delete_post_return_address(self,
                                   return_address_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| returnAddressId |  ``` Required ```  | Return address ID |



#### Example Usage

```python
return_address_id = 155

result = post_return_address_controller.delete_post_return_address(return_address_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="fax_controller"></a>![Class: ](https://apidocs.io/img/class.png ".FaxController") FaxController

### Get controller instance

An instance of the ``` FaxController ``` class can be accessed from the API Client.

```python
 fax_controller = client.fax
```

### <a name="fax_receipt_list"></a>![Method: ](https://apidocs.io/img/method.png ".FaxController.fax_receipt_list") fax_receipt_list

> Get List of Fax Receipts

```python
def fax_receipt_list(self)
```

#### Example Usage

```python

result = fax_controller.fax_receipt_list()

```


### <a name="get_fax_receipt"></a>![Method: ](https://apidocs.io/img/method.png ".FaxController.get_fax_receipt") get_fax_receipt

> Get a single fax receipt based on message id.

```python
def get_fax_receipt(self,
                        message_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageId |  ``` Required ```  | ID of the message receipt to retrieve |



#### Example Usage

```python
message_id = 'message_id'

result = fax_controller.get_fax_receipt(message_id)

```


### <a name="get_fax_history"></a>![Method: ](https://apidocs.io/img/method.png ".FaxController.get_fax_history") get_fax_history

> Get a list of Fax History.

```python
def get_fax_history(self,
                        date_from=None,
                        date_to=None,
                        q=None,
                        order=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| dateFrom |  ``` Optional ```  | Customize result by setting from date (timestsamp) Example: 1457572619. |
| dateTo |  ``` Optional ```  | Customize result by setting to date (timestamp) Example: 1457573000. |
| q |  ``` Optional ```  | Custom query Example: status:Sent,status_code:201. |
| order |  ``` Optional ```  | Order result by Example: date_added:desc,list_id:desc. |



#### Example Usage

```python
date_from = 155
date_to = 155
q = 'q'
order = 'order'

result = fax_controller.get_fax_history(date_from, date_to, q, order)

```


### <a name="calculate_price"></a>![Method: ](https://apidocs.io/img/method.png ".FaxController.calculate_price") calculate_price

> Calculate Total Price for Fax Messages sent

```python
def calculate_price(self,
                        fax_message)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| faxMessage |  ``` Required ```  | FaxMessageCollection model |



#### Example Usage

```python
fax_message = FaxMessageCollection()

result = fax_controller.calculate_price(fax_message)

```


### <a name="send_fax"></a>![Method: ](https://apidocs.io/img/method.png ".FaxController.send_fax") send_fax

> Send a fax using supplied supported file-types.

```python
def send_fax(self,
                 fax_message)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| faxMessage |  ``` Required ```  | FaxMessageCollection model |



#### Example Usage

```python
fax_message = FaxMessageCollection()

result = fax_controller.send_fax(fax_message)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="mms_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MMSController") MMSController

### Get controller instance

An instance of the ``` MMSController ``` class can be accessed from the API Client.

```python
 mms_controller = client.mms
```

### <a name="send_mms"></a>![Method: ](https://apidocs.io/img/method.png ".MMSController.send_mms") send_mms

> TODO: Add a method description

```python
def send_mms(self,
                 mms_messages)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| mmsMessages |  ``` Required ```  | MmsMessageCollection model |



#### Example Usage

```python
mms_messages = MmsMessageCollection()

result = mms_controller.send_mms(mms_messages)

```


### <a name="get_price"></a>![Method: ](https://apidocs.io/img/method.png ".MMSController.get_price") get_price

> Get Price for MMS sent

```python
def get_price(self,
                  mms_messages)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| mmsMessages |  ``` Required ```  | MmsMessageCollection model |



#### Example Usage

```python
mms_messages = MmsMessageCollection()

result = mms_controller.get_price(mms_messages)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="post_postcard_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PostPostcardController") PostPostcardController

### Get controller instance

An instance of the ``` PostPostcardController ``` class can be accessed from the API Client.

```python
 post_postcard_controller = client.post_postcard
```

### <a name="send_postcard"></a>![Method: ](https://apidocs.io/img/method.png ".PostPostcardController.send_postcard") send_postcard

> Send one or more postcards

```python
def send_postcard(self,
                      post_postcards)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| postPostcards |  ``` Required ```  | PostPostcard model |



#### Example Usage

```python
post_postcards = PostPostcard()

result = post_postcard_controller.send_postcard(post_postcards)

```


### <a name="calculate_price"></a>![Method: ](https://apidocs.io/img/method.png ".PostPostcardController.calculate_price") calculate_price

> Calculate price for sending one or more postcards

```python
def calculate_price(self,
                        post_postcards)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| postPostcards |  ``` Required ```  | PostPostcard model |



#### Example Usage

```python
post_postcards = PostPostcard()

result = post_postcard_controller.calculate_price(post_postcards)

```


### <a name="get_postcard_history"></a>![Method: ](https://apidocs.io/img/method.png ".PostPostcardController.get_postcard_history") get_postcard_history

> Retrieve the history of postcards sent or scheduled

```python
def get_postcard_history(self)
```

#### Example Usage

```python

result = post_postcard_controller.get_postcard_history()

```


### <a name="export_postcard_history"></a>![Method: ](https://apidocs.io/img/method.png ".PostPostcardController.export_postcard_history") export_postcard_history

> Export postcard history to a CSV file

```python
def export_postcard_history(self,
                                filename)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filename |  ``` Required ```  | Filename to export to |



#### Example Usage

```python
filename = 'filename'

result = post_postcard_controller.export_postcard_history(filename)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="upload_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UploadController") UploadController

### Get controller instance

An instance of the ``` UploadController ``` class can be accessed from the API Client.

```python
 upload_controller = client.upload
```

### <a name="upload_file"></a>![Method: ](https://apidocs.io/img/method.png ".UploadController.upload_file") upload_file

> Upload a file

```python
def upload_file(self,
                    file,
                    convert)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| file |  ``` Required ```  | The file to be uploaded |
| convert |  ``` Required ```  | The product that this file will be used with e.g. 'fax', 'mms', 'csv' or 'post' |



#### Example Usage

```python
file = open("pathtofile", 'rb')
convert = 'convert'

result = upload_controller.upload_file(file, convert)

```


### <a name="upload_file_1"></a>![Method: ](https://apidocs.io/img/method.png ".UploadController.upload_file_1") upload_file_1

> TODO: Add a method description

```python
def upload_file_1(self,
                      content,
                      convert)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| content |  ``` Required ```  | Base64-encoded file contents |
| convert |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
content = 'content'
convert = 'convert'

result = upload_controller.upload_file_1(content, convert)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="post_direct_mail_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PostDirectMailController") PostDirectMailController

### Get controller instance

An instance of the ``` PostDirectMailController ``` class can be accessed from the API Client.

```python
 post_direct_mail_controller = client.post_direct_mail
```

### <a name="location_search"></a>![Method: ](https://apidocs.io/img/method.png ".PostDirectMailController.location_search") location_search

> Search for a location

```python
def location_search(self,
                        country,
                        q)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| country |  ``` Required ```  | Country Code to search |
| q |  ``` Required ```  | Search term (e.g. post code, city name) |



#### Example Usage

```python
country = 'country'
q = 'q'

result = post_direct_mail_controller.location_search(country, q)

```


### <a name="send_campaign"></a>![Method: ](https://apidocs.io/img/method.png ".PostDirectMailController.send_campaign") send_campaign

> TODO: Add a method description

```python
def send_campaign(self,
                      post_direct_mail)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| postDirectMail |  ``` Required ```  | PostDirectMail model |



#### Example Usage

```python
post_direct_mail = PostDirectMail()

result = post_direct_mail_controller.send_campaign(post_direct_mail)

```


### <a name="calculate_price"></a>![Method: ](https://apidocs.io/img/method.png ".PostDirectMailController.calculate_price") calculate_price

> Calculate direct mail campaign price

```python
def calculate_price(self,
                        post_direct_mail)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| postDirectMail |  ``` Required ```  | PostDirectMail model |



#### Example Usage

```python
post_direct_mail = PostDirectMail()

result = post_direct_mail_controller.calculate_price(post_direct_mail)

```


### <a name="campaigns"></a>![Method: ](https://apidocs.io/img/method.png ".PostDirectMailController.campaigns") campaigns

> Get direct mail campaigns

```python
def campaigns(self)
```

#### Example Usage

```python

result = post_direct_mail_controller.campaigns()

```


[Back to List of Controllers](#list_of_controllers)



