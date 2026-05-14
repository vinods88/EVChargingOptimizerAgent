# EVChargingOptimizerAgent
This is a very basic agent created to understand the flow of "creating agents". This agent will output an EV charging schedule optimized for cost.

**Pre-requisites:**
1. Use any IDE that supports Python. I have used Google Colab eventhough I had python locally installed.
2. Access to any LLM API. Here I have used OpenAI API and with GPT 5.5. I had purchased 5$ worth of tokens to access the API. In case you will be using a different LLM, the call methods and the model name need to be changed in the code
3. URL for an API that provides live electricity prices for the region of interest

**Design:**
1. The agent will take inputs regarding the vehicle state:
  a. Current SOC of the battery
  b. Whether the Charger is plugged in
  c. Battery Capacity
  d. Target SOC
2. The agent will fetch electricity prices from Elpriset API for the the current day and the next day. The prices fetched are for a 15 minute window, so the agent will use an average value for hourly prices
3. The agent will calculate the amount of energy that the battery needs to be charged with and also the corresponding cost. The agent will explain the decision flow and the charging schedule along with the cost


