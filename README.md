<a href="https://996.icu"><img src="https://img.shields.io/badge/link-996.icu-red.svg" alt="996.icu" /></a>

IDE:
I'm using IntelliJ, you should be able to import the project easily.

Run:
This is a maven project, to run it, change directory to project root folder and run command: mvn package && java -jar target/stockdata-1.0-SNAPSHOT.jar

Check output:
type in browser: http://localhost:8080/getMaxProfitDates?stock=IBM, the output should like this:
{"status":{"code":200,"message":"Success."},"buyDate":"2017-08-21","sellDate":"2017-10-23","maxProfit":21.871399999999994}

Data source:
You can check the stock data from 3rd-party website by this url:
https://marketdata.websol.barchart.com/getHistory.json?apikey=1ab9d5c67b2b35fc622bb63e686eaa27&symbol=IBM&type=daily&startDate=20170501

data source url and data of how many days are configurable in application.properties file

Tests:
StockServiceTest.testCalculateMaxDiffIndexs is the main part to test the algorithm with different price input
StockControllerTest is testing web service(http) layer.
StockServiceTest mainly testing service layer and the algorithm.
