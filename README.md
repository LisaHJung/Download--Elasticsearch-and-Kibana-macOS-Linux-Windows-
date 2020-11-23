# Downloading Elasticsearch and Kibana

The Elastic Stack which consists of Elasticsearch, Kibana, Beats, and Logstash is **free and open**. 

The following links will take you to the download pages for Elasticsearch and Kibana.
* [Elasticsearch](https://www.elastic.co/downloads/elasticsearch)
* [Kibana](https://www.elastic.co/downloads/kibana?S_TACT=)

The directions for macOS/Linux and Windows are slightly different. Directions for both operatings systems are shown below. 
- [macOS and Linux](#for-macOS-and-linux)
- [Windows](#for-windows)

## For macOS and Linux

### Elasticsearch ###
**Step 1: Download Elasticsearch**

Go to [Elasticsearch](https://www.elastic.co/downloads/elasticsearch)download link.

Select the download option for your operating system(green box).
![Download ES](https://user-images.githubusercontent.com/60980933/99734881-d43ed480-2a80-11eb-807b-fa78198c94a1.jpg)

**Step 2: Relocate the downloaded Elasticsearch and extract it**

Where you relocate Elasticsearch is up to you but for this tutorial, I have moved it to the desktop. 

Once Elasticsearch is downloaded(orange box), control-click on Elasticsearch and click on show in folder. 
![Relocate the file](https://user-images.githubusercontent.com/60980933/99977274-a8ae3980-2d61-11eb-91c7-4210ef2b9acb.jpg)

Select the downloaded Elasticsearch(orange box) and move it to the desktop(green box). 
![Move to download](https://user-images.githubusercontent.com/60980933/99977759-4bff4e80-2d62-11eb-99ee-f65037032cbf.jpg)

Go to the desktop and unzip Elasticsearch by double clicking on it(orange box). 
![Unzip the file](https://user-images.githubusercontent.com/60980933/99979472-5d495a80-2d64-11eb-8e2d-0af00252e7f3.jpg)

**Step 3: Start the Elasticsearch server and ensure that everything is working properly**

By using the command line, we will locate the unzipped Elasticsearch folder in the desktop and run the Elasticsearch server!

Open up the terminal of choice. From your home directory, copy and paste the following command into your terminal to get to the Desktop. 
```
# In the terminal of your choice 
cd Desktop
```
Run the `ls` command in your terminal to look up the name of unzipped Elasticsearch folder(orange box) located in your Desktop. 
```
# In the terminal
ls
```
![Find ES on Desktop (1)](https://user-images.githubusercontent.com/60980933/99981789-1315a880-2d67-11eb-8a25-d80294e9eccc.jpg)

Change into the unzipped Elasticsearch directory.
```
# In the terminal
#The name of your unzipped Elasticsearch may differ from what is shown below. Make sure you cd into the right Elasticsearch directory. 
cd elasticsearch-7.10.0
```
You will see that you are now in the elasticsearch directory(orange box).
![CD into elasticsearch](https://user-images.githubusercontent.com/60980933/99982686-1e1d0880-2d68-11eb-908c-284f4c9e9eb5.jpg)

In the terminal, run the following command. 
```javascript
#In the terminal
bin/elasticsearch
```
You will see the cursor blinking for a while before you see Elasticsearch server running!
![Run ES](https://user-images.githubusercontent.com/60980933/99984221-05aded80-2d6a-11eb-8a92-212413abf8d8.jpg)

If you scroll down, you will see that Elasticsearch server is running on localhost at port 9200(orange box). 
![port 9200](https://user-images.githubusercontent.com/60980933/99984819-c633d100-2d6a-11eb-93d4-61dc0a2502b8.jpg)

A REST API is used to send a request to Elasticsearch server and the request is sent to the endpoint http://localhost:9200.

We will use cURL command line tool to check whether the request is received by Elasticsearch server.

Open up a NEW terminal. 

In the home directory of the new terminal, run the following command. 
```javascript
#In new terminal
curl http://localhost:9200
```
![curl command](https://user-images.githubusercontent.com/60980933/99986285-37c04f00-2d6c-11eb-9c05-0e48f2604630.jpg)

When you run the command(orange box), you will see the following JSON object displayed in your terminal(green box). That means everything is working correctly and Elasticsearch was successfully installed. 

Leave these two terminals open to keep the Elasticsearch server running. 

### Kibana ###

## For Windows 
### Elasticsearch ###
**Step 1: Download Elasticsearch**

Go to the download [link](https://www.elastic.co/downloads/elasticsearch).

In the region highlighted with a green box, select the download option for your operating system.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/jbfvm3lctmrnsjv3cw5o.png)

You will see that a zip file has been downloaded(orange box). 

If you scroll down the page, you will see the installation steps. We will be using the commands specified in these steps to test whether Elasticsearch server is running smoothly. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/4gv3340zhsuvwwqr87th.png)

**Step 2: Relocate the downloaded file and extract the file**
Where you relocate this file is up to you but for this tutorial, I have created a folder called Elastic_Stack in my Windows(C:) drive. 

Move the downloaded file to Elastic_Stack folder.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/19go5m3dcxv2wj9p0gnb.png)

Right click on the file to display pop up options and click on `extract all` option. Once the file has been extracted, double click on the file.  You will see the following displayed on your screen

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/svkdjodtmu95w1tpk9ti.png)

Double click on the file. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/x3r4nmeprirouzchsq8l.png)

Click on bin folder(red box). 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/isawkyt7vs8wzta8zenw.png)

Click on the region highlighted with a green box. It should reveal the file path to the bin folder. Copy this address. We will be using it in the next step. 

**Step 3: Start the Elasticsearch server and ensure that everything is working properly**

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ynudw1nktfk7qiaryjz3.png)

Search for the Command Prompt App on windows(purple box) and click on `run as administrator` option(red box). 

In the Command Prompt App terminal, change into the bin directory(cd) by providing the file path to the bin folder. This is the file path you have copied in the previous step.

```javascript
#In command prompt terminal
cd filepath to bin folder in Elasticsearch
```
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/rwbvh8g8g6iemh1u7f7z.png)

Red box highlights the command we have used to change to the bin directory. 

When you press enter, you will see that you have changed into the bin directory(blue box). 

In the terminal, run the following command. If you are running on a non-window OS, then run `elasticsearch` in the terminal instead. 

```javascript
#In command prompt terminal
elasticsearch.bat
```
You will see the cursor blinking for a while before you see Elasticsearch server running!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/zk1op2kd2zur6khdquj6.png)

You will see that Elasticsearch server is running on localhost at port 9200(red box). 

Let's recap real quick. When a user(client) sends a request to the server, the server sends a search query to the Elasticsearch server. A REST API is used to query the documents and this query is sent to the endpoint http://localhost:9200.

We will use cURL command line tool to check whether the request is received by Elasticsearch server.

Open up a new command prompt window(red box). 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/zbeyscea40g7bscnqjv8.png)

In the new terminal, run the following command. 
```javascript
#In new command prompt terminal
curl http://localhost:9200
```
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/fqrl0f2pwhcvoegbc9vp.png)

When you run the command(white box), you will see the following JSON object displayed in your terminal(blue box). That means everything is working correctly and Elasticsearch was successfully installed. 

Leave these terminals open to keep the Elasticsearch server running. 

### Kibana ###
Installing Kibana is very similar to installing Elasticsearch. 

**Step 1: Download Kibana**

Kibana is a web interface for Elasticsearch. However, it ships with its backend server that communicates with Elasticsearch. 

Go to the download [link](https://www.elastic.co/downloads/kibana).

In the region highlighted with a red box, select the download option for your operating system.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/pwjmemkhkgoxglr3mmo2.png)

You will see that a zip file has been downloaded. 

If you scroll down the page, you will see the installation steps. We will be using the commands specified in these steps to test whether Kibana server is running correctly. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/9odyrlqqs6rq4vbfoqfe.png)

**Step 2: Relocate the downloaded file and extract the file**
Move the downloaded file to Elastic_Stack folder.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/br6j8sbsclqk0az1gp6a.png)

Right click on the file to display options and click on `extract all` option. Once the file has been extracted, double click on the file.  

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ao50esqod7szl05y2jcf.png)

Click on bin folder(red box). 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/mf7q8t273mme9gbklyp6.png)

Click on the region highlighted with a green box. It should reveal the file path to the bin folder. Copy this address. We will be using it in the next step. 

**Step 3: Run Kibana and ensure that everything is working properly**

First, go back to the command prompt window that is running the Elasticsearch server. Make sure it is still running and it is not displaying any error messages. 

Open up a new command prompt window. 

In the Command Prompt App terminal, change into the bin directory(cd) of Kibana by providing the file path to the bin folder. This is the path you have copied from the bin folder in the previous step.

```javascript
#In command prompt terminal
cd filepath to bin folder in Kibana 
```
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/kimv9jgt3toyx31iwolz.png)

The command has been highlighted with a red box. 

When you press enter,you will see that you have changed into the bin directory(blue box). 

In the terminal, run the following command. If you are running on a non-window OS, then run `kibana` in the terminal instead. 

```javascript
#In command prompt terminal
kibana.bat
```
You will see the cursor blinking for a while before you see Kibana running!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/haaym56lxc2iyp6nhvgg.png)

Open up a browser and go to http://localhost:5601.

You will see the following displayed on the browser.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/hhutzyk8cxzvk3qi71ta.png)

**Troubleshooting**
```
If you are having trouble getting Kibana to work, try restarting your Elasticsearch server. Go to the command prompt terminal used for your Elasticserach server. Press `control + c`. Then, run elasticsearch.bat in the same terminal. 

Go back to your command prompt terminal for Kibana. Run `control + c` in the command prompt terminal. Then, run kibana.bat in the terminal. Go to http://localhost:5601 on your browser. 
```
All right let's get back to the Kibana browser.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/o8bsx564wkhhlvvj5kcj.png)

Click on the `menu` option(red box) to display a drop down menu. Scroll down to management section and click on `Dev Tools` option(green box). 

This tool allows us to easily send queries to Elasticsearch.  

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/p61s5ya2d537hi8fx3w0.png)
