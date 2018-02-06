# GROOVY Script
## Soap Test
###### TestSuite
> - GetProperties
> ```ruby
> //Test Suite Level Properties:
> def name = testRunner.testCase.testSuite.name;
> log.info("testRunner.testCase.testSuite.name:"+name);
> 
> def testSuiteName = testRunner.testCase.testSuite.name;
> log.info "Test Suite Properties [testRunner.testCase.testSuite.name]:\n$testSuiteName";
> def testSuiteProperties = testRunner.testCase.testSuite.properties;
> log.info "Test Suite Properties [testRunner.testCase.testSuite.properties]:\n$testSuiteProperties";
> def testSuitePropertiesName = testRunner.testCase.testSuite.getPropertyNames();
> log.info "Test Suite PropertiesName [testRunner.testCase.testSuite.getPropertyNames(]:\n$testSuitePropertiesName";
> ```

	
	
> - TestSuiteList
###### TestCase
> - GetProperties
> - TestCaseList
###### Project
> - GetProperties
> - ProjectListAllType
> - ProjectPath
###### TestStep
> - GetProperties
> - CurrentListTesStep
> - AllListTesStep
> - 1 - Request 1
> - RestTypePropertyStep
###### TestStepRun
> - TestStepRunGroovy
> - EnvironmentVariable
> - StackOverFlow.41551891
>```ruby
>
>def groovyUtils = new com.eviware.soapui.support.GroovyUtils( context );
>def testCase = testRunner.testCase;
>def testStep = null;
>def CC1 = testRunner.testCase.testSuite.getPropertyValue("CC1")
>log.info testRunner.testCase.testSuite.getPropertyValue("CC1")
>
>switch(CC1)  
>{  
>  case ~/^[H1]+$/: testStep = testCase.getTestStepByName( "PT02_H1" ); break;  
>  case ~/^[Y5]+$/: testStep = testCase.getTestStepByName( "PT02_Y5" ); break;  
>  case ~/^[Q2]+$/: testStep = testCase.getTestStepByName( "PT02_Q2" ); break;  
>  case ~/^[T5]+$/: testStep = testCase.getTestStepByName( "PT02_T5" ); break;  
>  default : testStep = testCase.getTestStepByName( "PT02_AQ" );  
>}
>testRunner = new com.eviware.soapui.impl.wsdl.testcase.WsdlTestCaseRunner(testCase, null);
>testStepContext = new com.eviware.soapui.impl.wsdl.testcase.WsdlTestRunContext(testStep);
>testStep.run(testRunner, testStepContext);
>log.info "TEST OK:"+testStep.getName();
>#http://stackoverflow.com/questions/41512276/running-specific-test-step-in-soapui-based-on-testsuite-property
>```

## File
###### File - CreateLoadPropeties
> - CreateFile
###### File - LoadFilePropeties
> - LoadFileProperty
###### File - DeleteFilePropeties
> - CreateFile
> - DeleteProperty
> - RemoveFile
## UISupport
###### Windows
> - PopUp-ComboBox
> - 1 - Request 1
> - Alert
