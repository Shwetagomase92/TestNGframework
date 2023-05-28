# TestNGframework
automating the business flow with rest assured API in that I use testNG framework and generate html report using allure.
This project is about how to automate the business flow with rest API by using the rest assured library along with the concepts of jsonpath and testNG assert.
I learned gradually and step by step and design our framework,
My framework is a combination of data driven and keyword driven framework. We have divided
the entire framework into three packages: The first package consists of common methods
wherein we have written common methods like excel data extractor,utility common function, request response file 
creator, excel data upgradation method and along with other methods. The second package 
consist of the classes corresponding to every test case. While the third package is nothing but the 
request repository.testng.xml is actually driving the entire execution.
                 Talking about how we have implemented our framework. The very first step is by using excel we 
have passed the request parameters on runtime for every test case, this is data dependent. We 
have written a small method which reads data from the corresponding test case from the excel 
sheet and creates a request on runtime in the request repository. Now this request repository is 
actually parameterized with variables for request parameters which are read from the excel 
sheet on runtime. Once the request is created the controls moves to the test case class. The test 
class consists of two parts, the first part is to validate the response status code. In our project 
there is environment limitation due to that sometimes request gets fail because of server not 
available or request time out. To avoid this issue what we have done is that first we are checking 
whether the response status code is equal to expected value or not. we add testng plugins and annotations @Test, @Before Test, @After tEST.test cases are run via testng.xml
we add dependency for allure and allure cmd, with the use of we drive our framework and after running allure results shows. allure cli takes files from allure result and generate allure report.
