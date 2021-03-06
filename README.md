# Downloading Elasticsearch and Kibana(macOS/Linux and Windows)

Elastic Stack consists of Elasticsearch, Kibana, Beats, and Logstash. 
Together, the Elastic Stack allows you to take data from any source, in any format, then search, analyze, and visualize it in real time.

Since the beginning, Elastic Stack has been **free and open!**

This repo will walk you through how you can download and run Elasticsearch and Kibana locally on Linux, macOS, or Windows. 

The following links will take you to the download pages for Elasticsearch and Kibana.
* [Elasticsearch](https://www.elastic.co/downloads/elasticsearch)
* [Kibana](https://www.elastic.co/downloads/kibana?S_TACT=)

The directions for macOS/Linux and Windows are slightly different. Directions for these operatings systems are shown below. 
- [macOS and Linux](#for-macOS-and-linux)
- [Windows](#for-windows)

If you want more in depth overview of Elasticsearch and Kibana, checkout my blog on [Beginner's guide to Elasticsearch](https://dev.to/lisahjung/beginner-s-guide-to-elasticsearch-4j2k). 

## For macOS and Linux

### Elasticsearch ###
**Step 1: Download Elasticsearch**

Go to the [Elasticsearch](https://www.elastic.co/downloads/elasticsearch) download link.

Select the download option for your operating system(green box).

![Download ES](https://user-images.githubusercontent.com/60980933/99734881-d43ed480-2a80-11eb-807b-fa78198c94a1.jpg)

**Step 2: Relocate the downloaded Elasticsearch and extract it**

Where you relocate Elasticsearch is up to you but for this tutorial, I am moving it to the desktop. 

Once Elasticsearch is downloaded(orange box), control-click on `Elasticsearch` and click on `show in folder`. 

![Relocate the file](https://user-images.githubusercontent.com/60980933/99977274-a8ae3980-2d61-11eb-91c7-4210ef2b9acb.jpg)

Select Elasticsearch(orange box) and move it to the desktop(green box). 

![Move to download](https://user-images.githubusercontent.com/60980933/99977759-4bff4e80-2d62-11eb-99ee-f65037032cbf.jpg)

Go to the desktop and unzip Elasticsearch by double clicking on it(orange box). Once Elasticsearch is unzipped, you will see a blue folder named Elasticsearch on your desktop. 

![Unzip the file](https://user-images.githubusercontent.com/60980933/99979472-5d495a80-2d64-11eb-8e2d-0af00252e7f3.jpg)

**Step 3: Start the Elasticsearch server and ensure that everything is working properly**

By using the command line, we will locate the unzipped Elasticsearch folder in the desktop and run the Elasticsearch server!

Open up a terminal of your choice. From your home directory, copy and paste the following command into your terminal to get to the Desktop. 
```
# In the terminal of your choice 
cd Desktop
```
Run the `ls` command in your terminal to check the name of your unzipped Elasticsearch folder(orange box) located in your Desktop. 
```
# In the terminal
ls
```
![Find ES on Desktop (2)](https://user-images.githubusercontent.com/60980933/99988145-8838ac00-2d6e-11eb-98f1-7c3b34fc82a0.jpg)

Change into the unzipped Elasticsearch directory by running the following command. 
```
# In the terminal
# A new version of Elasticsearch may have been released by the time you download Elasticsearch. 
#Therefore, the version of your download may differ from what is shown below(7.10.0). 
#Please make sure you cd into the Elasticsearch directory shown when using the ls command from the previous step.  

cd elasticsearch-7.10.0
```
You will see that you are now in the elasticsearch directory(orange box).

![CD into elasticsearch](https://user-images.githubusercontent.com/60980933/99982686-1e1d0880-2d68-11eb-908c-284f4c9e9eb5.jpg)

In the terminal, run the following command. 
```javascript
# In the terminal
bin/elasticsearch
```
You will see the cursor blinking for a while before Elasticsearch server starts running!
![Run ES](https://user-images.githubusercontent.com/60980933/99984221-05aded80-2d6a-11eb-8a92-212413abf8d8.jpg)

**Step 4: Send a cURL command to the Elasticsearch server to make sure that Elasticsearch is up and running**

A REST API is used to send requests to the Elasticsearch server. These requests are sent to the endpoint http://localhost:9200.

We will use a cURL command to check whether the request is received by Elasticsearch server.

Open up a NEW terminal. 

In the home directory of the new terminal, run the following command. 
```javascript
# In the new terminal
curl http://localhost:9200
```
![curl command](https://user-images.githubusercontent.com/60980933/99986285-37c04f00-2d6c-11eb-9c05-0e48f2604630.jpg)

When you run the command(orange box), you will see the following JSON object displayed in your terminal(green box). If you see this JSON object, that means everything is working correctly and Elasticsearch has been successfully installed. 

Leave these two terminals open to keep the Elasticsearch server running. 

### Kibana ###
Downloading Kibana is very similar to downloading Elasticsearch. 

**Step 1: Download Kibana**

Kibana is a web interface for Elasticsearch. Kibana ships with its backend server that communicates with Elasticsearch. 

Go to the [Kibana](https://www.elastic.co/downloads/elasticsearch) download link.

In the region highlighted with a red box, select the download option for your operating system.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/pwjmemkhkgoxglr3mmo2.png)

You will see that a zip file has been downloaded. 

**Step 2: Relocate the downloaded Kibana and extract it**

Where you relocate Kibana is up to you but for this tutorial, I am moving it to the desktop. 

Once Kibana is downloaded(orange box), control-click on `Kibana` and click on `show in folder`. 
![download Kibana](https://user-images.githubusercontent.com/60980933/99998021-4104e800-2d7b-11eb-8bfc-64f0d92299be.jpg)

Select the downloaded Kibana(orange box) and move it to the desktop(green box). 
![relocate kibana](https://user-images.githubusercontent.com/60980933/99998292-b07ad780-2d7b-11eb-8136-ba70ae8e22c7.jpg)

Go to the desktop and unzip Kibana by double clicking on it(orange box). Once Kibana is unzipped, you will see a blue folder named Kibana on your desktop. 

![unzip kibana](https://user-images.githubusercontent.com/60980933/99998479-fafc5400-2d7b-11eb-8004-48d9c7caa431.jpg)

**Step 3: Run Kibana and ensure that everything is working properly**

By using the command line, we will locate the unzipped Kibana folder in the desktop and run the Kibana server!

Open up a new terminal. From your home directory, copy and paste the following command into your terminal to get to the Desktop. 
```
# In a new terminal
cd Desktop
```
Run the `ls` command in your terminal to check the name of your unzipped Kibana folder(orange box) located in your Desktop. 
```
# In the terminal
ls
```
![cd into Kibana (1)](https://user-images.githubusercontent.com/60980933/99999182-013f0000-2d7d-11eb-9eb9-1e2a5a7764ab.jpg)

Change into the unzipped Kibana directory.
```
# In the terminal
# By the time you download Kibana, a new version of Kibana may have been released. 
# Therefore, the version of your download may differ from what is shown below(7.10.0-darwin-x86_64). 
# Please make sure you cd into the Kibana directory shown when using the ls command from the previous step.  

cd kibana-7.10.0-darwin-x86_64
```
You will see that you are now in the Kibana directory(orange box).

![Kibana directory](https://user-images.githubusercontent.com/60980933/100003785-dc01c000-2d83-11eb-9077-47438e7fc195.jpg)

In the terminal, run the following command. 
```javascript
# In the terminal
bin/kibana 
```
You will see the cursor blinking for a while before you see Kibana running!

![Kibana running](https://user-images.githubusercontent.com/60980933/100004159-57fc0800-2d84-11eb-98c4-5c1c5f807015.jpg)

When you see the following message that the `Server is running at http://localhost:5601` in your terminal, you are ready to work with the Kibana interface. 

![Kibanna server running ](https://user-images.githubusercontent.com/60980933/100004309-8c6fc400-2d84-11eb-8651-08cb95217152.jpg)

Open up a browser and go to http://localhost:5601.

You will see the following displayed on the browser.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/hhutzyk8cxzvk3qi71ta.png)

**If Kibana does not load on your browser...**
```
If you are having trouble getting Kibana to load, try restarting your Elasticsearch server. 
Go to the terminal used for your Elasticserach server. 
Press control + c. Then, run bin/elasticsearch in the same terminal. 

Go back to your terminal that is running Kibana. 
Run control + c in the command prompt terminal. 
Then, run bin/kibana in the terminal. Go to http://localhost:5601 on your browser. 
```
All right let's get back to the Kibana browser.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/o8bsx564wkhhlvvj5kcj.png)

Click on the `menu` option(red box) to display a drop down menu. Scroll down to management section and click on `Dev Tools` option(green box). 

You will see the following interface here where you can send search queries to Elasticsearch!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/p61s5ya2d537hi8fx3w0.png)

Congrats. You have successfully downloaded and ran Elasticsearch and Kibana on your macOS/Linux!

## For Windows 
### Elasticsearch ###
**Step 1: Download Elasticsearch**

Go to the [Elasticsearch](https://www.elastic.co/downloads/elasticsearch) download link.

In the region highlighted with a green box, select the download option for Windows. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/jbfvm3lctmrnsjv3cw5o.png)

You will see that a zip folder has been downloaded(orange box). 

**Step 2: Relocate the downloaded Elasticsearch and extract it**

Where you relocate this file is up to you but for this tutorial, I have created a folder called Elastic_Stack in my Windows(C:) drive. 

Move the downloaded file to Elastic_Stack folder.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/19go5m3dcxv2wj9p0gnb.png)

Right click on the folder to display pop up options and click on `extract all` option. Once the folder has been extracted, double click on the folder.  You will see the following displayed on your screen.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/svkdjodtmu95w1tpk9ti.png)

Double click on the folder. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/x3r4nmeprirouzchsq8l.png)

Click on bin folder(red box). 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/isawkyt7vs8wzta8zenw.png)

Click on the region highlighted with a green box. It should reveal the file path to the bin folder. Copy this address. We will be using it in the next step. 

**Step 3: Start the Elasticsearch server and ensure that everything is working properly**

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ynudw1nktfk7qiaryjz3.png)

Search for the Command Prompt App in the search bar(purple box) and click on `run as administrator` option(red box). 

In the Command Prompt App terminal, change into the bin directory(cd) by providing the file path to the bin folder. This is the file path you have copied in the previous step.

```javascript
# In the command prompt terminal

cd filepath to bin folder in Elasticsearch
```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/rwbvh8g8g6iemh1u7f7z.png)

Red box highlights the command we have used to change to the bin directory. 

When you press enter, you will see that you have changed into the bin directory(blue box). 

In the terminal, run the following command.

```javascript
# In the command prompt terminal

elasticsearch.bat
```
You will see the cursor blinking for a while before Elasticsearch server starts running!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/zk1op2kd2zur6khdquj6.png)

You will see that Elasticsearch server is running on localhost at port 9200(red box). 

A REST API is used to send a request to the Elasticsearch server. The request is sent to the endpoint http://localhost:9200.

We will use a cURL command to check whether the request is received by Elasticsearch server.

Open up a new command prompt window(red box). 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/zbeyscea40g7bscnqjv8.png)

In the new terminal, run the following command. 
```javascript
# In new command prompt terminal

curl http://localhost:9200
```
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/fqrl0f2pwhcvoegbc9vp.png)

When you run the command(white box), you will see the following JSON object displayed in your terminal(blue box). That means everything is working correctly and Elasticsearch has been successfully installed. 

Leave these terminals open to keep the Elasticsearch server running. 

### Kibana ###
Installing Kibana is very similar to installing Elasticsearch. 

**Step 1: Download Kibana**

Kibana is a web interface for Elasticsearch. Kibana ships with its backend server that communicates with Elasticsearch. 

Go to the [Kibana](https://www.elastic.co/downloads/kibana) download link. 

In the region highlighted with a red box, select the download option for Windows. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/pwjmemkhkgoxglr3mmo2.png)

You will see that a zip folder has been downloaded. 

**Step 2: Relocate the downloaded Kibana and extract it**

Where you relocate this folder is up to you but for this tutorial, I have created a folder called Elastic_Stack in my Windows(C:) drive.

Move the downloaded folder to Elastic_Stack folder.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/br6j8sbsclqk0az1gp6a.png)

Right click on the folderto display options and click on `extract all` option. Once the folder has been extracted, double click on the folder.  

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ao50esqod7szl05y2jcf.png)

Click on the bin folder(red box). 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/mf7q8t273mme9gbklyp6.png)

Click on the region highlighted with a green box. It should reveal the file path to the bin folder. Copy this address. We will be using it in the next step. 

**Step 3: Run Kibana and ensure that everything is working properly**

First, go back to the command prompt window that is running the Elasticsearch server. Make sure it is still running and it is not displaying any error messages. 

Open up a new command prompt window. 

In the Command Prompt App terminal, change into the bin directory(cd) of Kibana by providing the file path to the bin folder. This is the path you have copied from the bin folder in the previous step.

```javascript
# In the command prompt terminal

cd filepath to bin folder in Kibana 
```
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/kimv9jgt3toyx31iwolz.png)

The command has been highlighted with a red box. 

When you press enter, you will see that you have changed into the bin directory(blue box). 

In the terminal, run the following command. 

```javascript
# In the command prompt terminal

kibana.bat
```
You will see the cursor blinking for a while before you see Kibana running! 
When you see the message `http server running at http://localhost:5601` in your terminal, you are ready to work with the Kibana interface. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/haaym56lxc2iyp6nhvgg.png)

Open up a browser and go to http://localhost:5601.

You will see the following displayed on the browser.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/hhutzyk8cxzvk3qi71ta.png)

**If Kibana does not load on your browser...**
```
If you are having trouble getting Kibana to load, try restarting your Elasticsearch server. 
Go to the terminal used for your Elasticserach server. 
Press control + c. Then, run elasticsearch.bat in the same terminal. 

Go back to your terminal that is running Kibana.
Run control + c in the command prompt terminal. 
Then, run kibana.bat in the terminal. 
Go to http://localhost:5601 on your browser. 
```
All right let's get back to the Kibana browser.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/o8bsx564wkhhlvvj5kcj.png)

Click on the `menu` option(red box) to display a drop down menu. Scroll down to management section and click on `Dev Tools` option(green box). 

You will see the following interface here where you can send search queries to Elasticsearch!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/p61s5ya2d537hi8fx3w0.png)

Congrats. You have successfully downloaded and ran Elasticsearch and Kibana on Windows!
