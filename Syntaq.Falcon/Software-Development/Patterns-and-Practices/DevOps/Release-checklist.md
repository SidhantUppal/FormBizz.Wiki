We want to ensure our clients get the best experience, in order to provide this we want to make sure that any release is bug free. We ensure the releases are bug free through user testing and running our automated unit and functional tests. 

Because the platform is highly customisable we need to supplement the user testing of a feature with additional tests. There are outlined below:

1. Run Component Check forms from the portal [form access](https://syntaq-falcon-preprod-test.azurewebsites.net/Falcon/forms/load?OriginalId=c92f0699-f52b-49d8-8af6-c46ad4d0e0f9&version=live)
2. Run the Component Check embedded forms from the demo.syntaq website  [form access](https://demo.syntaq.com/falcontest/component-check)
3. Verifying Hydro SSO configuration
4. Configuration of profiles (build configuration testing) i.e. compile time switches MBIE and Falcon branches considering we are maintain a single code base. 
5. Testing is not just done on a admin users we need to consider other profiles like "users" or author
6. ensure we are not resolving back to local host. 

Check your code before you deploy
1. Remove all debug