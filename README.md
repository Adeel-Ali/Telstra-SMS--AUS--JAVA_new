# Getting Started
## How to Build

The generated code uses a few Maven dependencies e.g., Jackson, UniRest,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for successful build.

* In order to open the client library in Eclipse click on ``` File -> Import ```.

![Importing SDK into Eclipse - Step 1](http://apidocs.io/illustration/java?step=import0&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

* In the import dialog, select ``` Existing Java Project ``` and click ``` Next ```.

![Importing SDK into Eclipse - Step 2](http://apidocs.io/illustration/java?step=import1&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

* Browse to locate the folder containing the source code. Select the detected location of the project and click ``` Finish ```.

![Importing SDK into Eclipse - Step 3](http://apidocs.io/illustration/java?step=import2&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](http://apidocs.io/illustration/java?step=import3&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

## How to Use

The following section explains how to use the TelstraSMSAUS library in a new console project.     
    
#### 1. Starting a new project
For starting a new project, click the menu command ``` File > New > Project ```.

![Add a new project in Eclipse](http://apidocs.io/illustration/java?step=createNewProject0&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

Next, choose ``` Maven > Maven Project ```and click ``` Next ```.

![Create a new Maven Project - Step 1](http://apidocs.io/illustration/java?step=createNewProject1&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

Here, make sure to use the current workspace by choosing ``` Use default Workspace location	```, as shown in the picture below and click ``` Next ```.

![Create a new Maven Project - Step 2](http://apidocs.io/illustration/java?step=createNewProject2&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

Following this, select the *quick start* project type to create a simple project with an existing class and a ``` main ``` method. To do this, choose ``` maven-archetype-quickstart ``` item from the list and click ``` Next ```.

![Create a new Maven Project - Step 3](http://apidocs.io/illustration/java?step=createNewProject3&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

In the last step, provide a ``` Group Id ``` and ``` Artifact Id ``` as shown in the picture below and click ``` Finish ```.

![Create a new Maven Project - Step 4](http://apidocs.io/illustration/java?step=createNewProject4&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)


#### 2. Add reference of the library project
The created Maven project manages its dependencies using its ``` pom.xml ``` file. In order to add a dependency on the *TelstraSMSAUSLib* client library, double click on the ``` pom.xml ``` file in the ``` Package Explorer ```. Opening the ``` pom.xml ``` file will render a graphical view on the cavas. Here, switch to the ``` Dependencies ``` tab and click the ``` Add ``` button as shown in the picture below.

![Adding dependency to the client library - Step 1](http://apidocs.io/illustration/java?step=testProject0&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

Clicking the ``` Add ``` button will open a dialog where you need to specify TelstraSMSAUS in ``` Group Id ``` and TelstraSMSAUSLib in the ``` Artifact Id ``` fields. Once added click ``` OK ```. Save the ``` pom.xml ``` file.

![Adding dependency to the client library - Step 2](http://apidocs.io/illustration/java?step=testProject1&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

#### 3. Write sample code
Once the ``` SimpleConsoleApp ``` is created, a file named ``` App.java ``` will be visible in the *Package Explorer* with a ``` main ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Adding dependency to the client library - Step 2](http://apidocs.io/illustration/java?step=testProject2&workspaceFolder=Telstra SMS (AUS)-Java&workspaceName=TelstraSMSAUS&projectName=TelstraSMSAUSLib&rootNamespace=com.telstra.api)

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project *TelstraSMSAUSLib* from the package explorer.
2. Select "Run -> Run as -> JUnit Test" or use "Alt + Shift + X" followed by "T" to run the Tests.

## Initialization

#### Authentication and Initialization
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | The OAuth 2.0 access token to be set before API calls |



API client can be initialized as following.

```java
// Initializing Object Mapper for Serialization and Deserialization purposes
public static ObjectMapper mapper = new ObjectMapper()
{
	private static final long serialVersionUID = -174113593500315394L;
	{
		configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);
		setSerializationInclusion(JsonInclude.Include.NON_NULL);
	}
};

// Configuration parameters and credentials
String oAuthAccessToken = "oAuthAccessToken"; // The OAuth 2.0 access token to be set before API calls

TelstraSMSAUSClient client = new TelstraSMSAUSClient(oAuthAccessToken);
```

# Class Reference
## <a name="list_of_controllers"></a>List of Controllers

* [APIController](#api_controller)

## <a name="api_controller"></a>![Class: ](http://apidocs.io/img/class.png "com.telstra.api.controllers.APIController") APIController

#### Get singleton instance
The singleton instance of the ``` APIController ``` class can be accessed from the API Client.
```java
APIController client = client.getClient();
```

### <a name="get_message_status_async"></a>![Method: ](http://apidocs.io/img/method.png "com.telstra.api.controllers.APIController.getMessageStatusAsync") getMessageStatusAsync

> Use the unique identifier (messageId) returned as returned in the response from the Send SMS method to get the status

```java
void getMessageStatusAsync(
        final String messageID,
        final APICallBack<MessageStatus> callBack)
```

#### Parameters: 

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageID |  ``` Required ```  | The unique id representing the message request |



#### Example Usage:
```java
String messageID = "messageID";
// Invoking the API call with sample inputs
client.getMessageStatusAsync(messageID, new APICallBack<MessageStatus>() {
    public void onSuccess(HttpContext context, MessageStatus response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```





### <a name="create_sms_message_async"></a>![Method: ](http://apidocs.io/img/method.png "com.telstra.api.controllers.APIController.createSMSMessageAsync") createSMSMessageAsync

> Send an SMS to an AUS mobile, returns A unique identifier for the SMS response  (messageId) 

```java
void createSMSMessageAsync(
        final SendMessageRequest messageRequest,
        final APICallBack<SendMessageResponse> callBack)
```

#### Parameters: 

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageRequest |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage:
```java
try {
    SendMessageRequest messageRequest = new SendMessageRequest();
    // Invoking the API call with sample inputs
    client.createSMSMessageAsync(messageRequest, new APICallBack<SendMessageResponse>() {
        public void onSuccess(HttpContext context, SendMessageResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```





### <a name="get_authentication_async"></a>![Method: ](http://apidocs.io/img/method.png "com.telstra.api.controllers.APIController.getAuthenticationAsync") getAuthenticationAsync

> *Tags:*  ``` Skips Authentication ``` 

> Get an Oauth Token

```java
void getAuthenticationAsync(
        final GetAuthenticationInput input,
        final APICallBack<AuthenticationResponse> callBack)
```

#### Parameters: 

| Parameter | Tags | Description |
|-----------|------|-------------|
| clientId |  ``` Required ```  | TODO: Add a parameter description |
| clientSecret |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage:
```java
GetAuthenticationInput collect = new GetAuthenticationInput();

String clientId = "client_id";
collect.setClientId(clientId);

String clientSecret = "client_secret";
collect.setClientSecret(clientSecret);

// Invoking the API call with sample inputs
client.getAuthenticationAsync(collect, new APICallBack<AuthenticationResponse>() {
    public void onSuccess(HttpContext context, AuthenticationResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```





### <a name="get_message_response_async"></a>![Method: ](http://apidocs.io/img/method.png "com.telstra.api.controllers.APIController.getMessageResponseAsync") getMessageResponseAsync

> The recipients of your SMS messages can send a reply which you can retrieve using the Get Message Response method. Pass through the unique identifier (messageId) returned as returned in the response from the Send SMS method and you will receive the reply and the timestamp.

```java
void getMessageResponseAsync(
        final String messageID,
        final APICallBack<ResponseStatusEnum> callBack)
```

#### Parameters: 

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageID |  ``` Required ```  | the unique id of the message request |



#### Example Usage:
```java
String messageID = "messageID";
// Invoking the API call with sample inputs
client.getMessageResponseAsync(messageID, new APICallBack<ResponseStatusEnum>() {
    public void onSuccess(HttpContext context, ResponseStatusEnum response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```





[Back to List of Controllers](#list_of_controllers)


