# LimaCharlie Lab

part 1/2

In this lab we will be using LimaCharlie to investigate endpoint monitoring and threat detection.

What is Lima Charlie? Lima Charlie is a lightweight browser based tool, that is great for big and small organizations, It helps keep an eye on systems, detect threats, and responds quickly to any suspicious activity.
This walktrhough will be using the chrome browser, however any browser can be used.

To start, lets open a browser window. 

Once the window is up, navigate to the following URL:

`https://app.limacharlie.io/login`

When the webpage loads, Click "Create an account"

![](attachments/register_an_account.PNG)

The screen will change slightly as it asks you which method you would like to use to sign-up with. 

We selected "Sign up with email"

![](attachments/LimaCharlie_signupmethod.png)

Fill out the fields click the "Sign Up" button to continue

![](attachments/SIGN_UP_BUTTON.PNG)

Then go to your email and you should recieve a link to verify your account. Click the link and then go back to your browser and refresh the page.

Once you return to your page you should see Lima Charlie asking you some questions about your company, you can create any fake company you wish.

Enter the following answers into there respective fields ->

* <span style="color:green">What best describes your team/company?</span> -> Security Operations Center
* <span style="color:red">What best describes your role?</span> -> Security Engineer
* <span style="color:blue">What use cases are you exploring?</span> -> Endpoint detection & Response
* <span style="color:yellow">How did you hear about us?</span> -> Black Hills Info Sec

![](attachments/company_setup_menu.PNG)

Once those fields are filled, check the box that says "By checking this box, I hereby agree and consent to the Terms of Service and Privacy Policy."

Click "Get Started"

Then click "Create Organization" 

![](attachments/create_an_organization.PNG)

Then you can enter the following information into the fields, you create your fictional organization.

![](attachments/ficticious_company_selection.PNG)

Click Create Organization.

There may be be a small delay while Lima Charlie creates the new company.

It is possible to use this tool to manage more than one company or organization at a time.

Once the page finishes loading you will see a menu like the one below. 

Please select your company. 

Note: if you dont see this, move on to the next step.

![](attachments/selectorganization.png)

Once you have selected your ficticious company, you can look around and see all the options that this tool has too offer.

For this demonstration we will be creating a sensor for our windows machine and then setting off atomic red to test if our filter catches it.

On the left side under sensors, please select "Installation Keys"

![](attachments/one.PNG)

You should then see an option in the center "Create Installation key", Select it

![](attachments/two.PNG)

Then you will see a few empty fields, You can add any description you like and any relevant tags.

Once you have done that you can select "Create"

![](attachments/three.PNG)

Once you have created your new installation key you can navigate too "Sensors List" and click "Add Sensor"

![](attachments/four.PNG)

![](attachments/addsensor.png)

Scroll down and select the "Windows" sensor.

![](attachments/five.PNG)

Once you select windows you will be greeted with an installation key menu. Once here select from the drop down menu the description you created earlier for your installation key. And then click "Select"

![](attachments/six.PNG)

You will then be prompted with what architecture to download, every windows machine may be different but in our case, "86-64 exe"should be right.

![](attachments/seven.PNG)

Once you do that you will be greeted with a few more steps to creating your endpoint. First, click "Download the selected installer", once thats finished downloading copy the string in step 4 to your clipboard.

![](attachments/eight.PNG)

Then you need to go to your desktop, right click "Windows Terminal" and select "run as administrator"

![](attachments/nine.PNG)

Next, run the following command to get into the downloads directory

<pre>cd .\Downloads</pre>

Now we are going to enter the beginning of our next command.
Tab completion is your friend!

<pre>.\hcp_win_x64_release_4.29.2.exe [RIGHT CLICK OR CTL+V TO PASTE]</pre>

After starting the command, we will paste the string we copied to our clipboard. 

Once the string has been pasted into the command, go ahead and hit enter to run it. 

If done correctly, your output should look like this:

![](attachments/correctoutput.png)

Now, return to the browser window. You should see this message:

![](attachments/success.PNG)

Please note that the name of your computer will be different!

<a href="https://github.com/strandjs/IntroLabs/blob/master/IntroClassFiles/Tools/IntroClass/LCmeetsAtomicRed/LCAR.md">Part 2</a>
