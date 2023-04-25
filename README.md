# image-lambda

[images.json](https://lab17-kirk.s3.us-west-2.amazonaws.com/images.json)  

My lambda is automatically used when I add an image to my s3. When that happens the lambda picks up the event, and logs the image size and name in the images.json file. It creates a new file if it doesn't exist.  

Problems encountered:  
- need to remember to JSON.stringify things to send them up in a put request  
- having the correct file name in the trigger, for example images/ vs Images/ doesn't get you to the same place  
- my array was first set to null, and that stopped the .json from updating. Once I changed that it worked
