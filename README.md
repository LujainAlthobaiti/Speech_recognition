# Voice_Recognition
using an online HTML editor to create speech recognition. 

# Voice Recognition:

 A straightforward implementation of speech recognition capabilities on a web page is shown by the supplied HTML code snippet. With the help of this code, users will be able to speak text into an input field, which will subsequently be translated and displayed as text.

# HTML Structure:

The HTML structure is straightforward. It consists of a basic structure with a section. Within the section, necessary meta information and the title of the webpage are defined. The section contains the input field and the JavaScript code responsible for speech recognition.


# Input Area:

An input field is created using the <input> element with a type of "text". The label "Speech Recognition" is associated with the input field, which is intended to capture user input using speech. The placeholder attribute provides a hint to users about what type of input is expected. Additionally, the onclick attribute is assigned to the input field, linking it to the JavaScript function named record().

# JavaScript Code:

The JavaScript code embedded within the <script> tags defines the record() function. This function is invoked when the input field is clicked. Here's a breakdown of the code inside the record() function: 

A new instance of the webkitSpeechRecognition class is created and assigned to the recognition variable. This class is a built-in browser API for speech recognition.
The lang property of the recognition object is set to "en-GB", indicating that the recognition will be performed using British English.
The onresult event handler is defined for the recognition object. This handler is triggered when speech is recognized.
Inside the event handler, the recognized speech data is retrieved from the event.results object. The text transcript of the recognized speech is extracted from event.results[0][0].transcript.
The extracted transcript is then used to set the value of the input field using document.getElementById('speechToText').value.

# Overall Functionality:

When the user clicks the input field labeled "Speech Recognition," the record() function is triggered. The browser's speech recognition functionality is initiated, and the user's speech input is processed. Once the recognition is successful, the transcribed text is displayed in the same input field, replacing the placeholder text.

# Conclusion:

In conclusion, this code sample illustrates a fundamental JavaScript implementation of voice recognition in a web page. Users may talk into their device's microphone and then click the input box to have their spoken words translated into text. This approach may be used as a starting point for user interfaces and complex voice recognition applications.

# Tutorialspoint website:

 There are other websites available, however the one I recommend is found at this link:
   [link](https://www.tutorialspoint.com/online_html_editor.php)

# HTML Code:

    <!DOCTYPE html>
    <html lang="en">

    <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <meta http-equiv="X-UA-Compatible" content="ie=edge">
     <title>Document</title>
    </head>

    <body>
     <!-- Input area -->
     <label for="Speech Recognition">Speech Recognition</label>
     <input type="text" name="" id="speechToText" placeholder="Speak Something" onclick="record()">

     <!-- Below is the script for voice recognition and conversion to text-->
    <script>
        function record() {
            var recognition = new webkitSpeechRecognition();
            recognition.lang = "en-GB";

            recognition.onresult = function(event) {
                // console.log(event);
                document.getElementById('speechToText').value = event.results[0][0].transcript;
            }
            recognition.start();

        }
    </script>
    <!-- end of script -->
    </body>

    </html>
    
# OutPut ScreenShot:

  ![photo](outPut.png)
  
# Simulation:

 You can launch the project's simulation by clicking this link:
 [link](http://tpcg.io/TYGJMX)
