# Mono2Micro  
  
  ## Main resources links
  https://www.ibm.com/docs/mono2micro  
  https://developer.ibm.com/tutorials/transform-monolithic-java-applications-into-microservices-with-the-power-of-ai/  
  https://ibm.ent.box.com/v/Mono2Micro-Workshop-Lab  
  https://developer.ibm.com/articles/a-non-disruptive-approach-to-transform-java-monoliths-to-microservices/  
  https://www.youtube.com/watch?v=vN67fi1Yc0o  
  
  
  ## Download installer and quick start files
  
  Download these files:  
  http://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/mono2micro/Mono2Micro-Monolith-DataCollector.zip?_ga=2.75269265.2042933619.1641982899-396393358.1641521770
  http://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/mono2micro/Mono2Micro-Example.zip?_ga=2.83747989.2042933619.1641982899-396393358.1641521770
  
  Pull these docker images
  ```
  docker pull ibmcom/mono2micro-bluejay
  docker pull ibmcom/mono2micro-aipl
  docker pull ibmcom/mono2micro-ui
  docker pull ibmcom/mono2micro-cardinal
  ```
  ## Tutorial Steps
  
  1. Create directory /m2m
  2. Unzip Mono2Micro-example.zip and Mono2Micro-Monolith-DataCollector.zip to /m2m directory
  3. Run the Mono2Micro Bluejay tool to analyze the Java source code, instrument it, and produce the analysis in two JSON files. 
  ```
  docker run -e LICENSE=accept --rm -it -v /m2m/daytrader:/var/application ibmcom/mono2micro-bluejay /var/application/monolith
  ```
  4. Run the flicker tool  
  Flicker is a simple Java-based tool that prompts the user for the use label and then records the start time, and prompts again for the “stop” command after the user finishes running that scenario on the monolithic application.
  ```
  java -cp commons-net-3.6.jar;json-simple-1.1.jar;. Flicker -no_ntp
  ```
  5. adf

  
  
  
  
  
