# Video Tracking with Marketo Munchkin

This is a guide to setting up video hosting sites YouTube and Wistia to work with the Marketo Munchkin API, and log whenever a video is played to the Marketo activity log. This is handy because it allows you to not only see that someone visited a page that a video is embedded on, but also that the video was actually played. You can then use this to create interesting moments, log a program success, or even trigger follow up actions like an email.

Below are the steps to take in setting up these scripts to track properly:

#Using Munchkin API to track embedded video behavior

A common need among Marketo users lies in the ability to track embedded video engagement with their prospects and customers. Marketo will natively track form submissions and web page activity, but it does not have built-in video tracking functionality (save for the functionality within the social media module). 

Since it’s important for marketers to understand when their target audiences actually view or interact in a certain way with a video, and not just that they visited a web page that happened to have a video on it, a more robust solution is needed.

By leveraging Marketo’s munchkin API in conjunction with an API-enabled video hosting service like YouTube or Wistia, it’s easy to build this integration yourself. Don’t get too scared off by terms like API- this particular piece of functionality is actually pretty simple to implement with a basic understanding of HTML and Marketo.

Before we get into the specifics of how this works, you’ll first need to set up your Marketo instance to use the Munchkin API. Marketo Admins should first navigate to their admin section > Integration > Munchkin > Edit API Configuration. You’ll want to check the box labeled “Enable Munchkin API”. If your API Private Key is blank, don't worry about it--you won't need it here.
 
Now that you have this squared away, you’re set to start setting up your customized embed code. I've included types of embed codes, depending on the site you're hosting your videos on. YouTube is widely accessible, but I've found it sometimes gets blocked by cor orate IT filters, so I've been using Wistia more lately. 

# Embedding with Wistia

1.	Your video ID (10 digit code that you can find in the embed code on Wistia, or on the video URL)
2.	Video height and width dimensions (eg 550x309)

Next, you’ll need a landing page to embed your video to. Generally it’s advisable to do this within a program so that you can make use of the token-enabled script, however if you’re comfortable editing the script yourself and cannot make use of program tokens, you can install the videos on really any landing page.

I've included two versions of the Wistia script: one with tokens for key variables (recommended) and one that does not use tokens. The difference here is that the token-enabled script can have variables edited at 

Below are the scripts you’ll want to place within an HTML object on a marketo landing page. Note: You do not need to also use the embed code that can usually be obtained from YouTube or Wistia directly. The scripts below will handle both the embed of the video and the tracking and integration with Marketo. 
