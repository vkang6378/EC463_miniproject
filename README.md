# EC463_miniproject
Frontend: 

The frontend of our Flask application is structured using a combination of Python code and HTML templates. The Python file forms.py contains two classes RegistrationForm and LoginForm, each defining fields with validators to ensure that the user input meets certain criteria. For the frontend display, HTML templates are used, which are located in the templates directory. When a user navigates to the registration or login page, Flask serves the corresponding HTML template, integrating the form fields as defined in forms.py. The main.css file contains the CSS rules that are applied to the HTML templates to ensure that the forms and other elements on the frontend are displayed properly and are visually appealing.

Results:
![image](https://github.com/vkang6378/EC463_miniproject/assets/75413432/52c66b67-4989-40a4-8368-4d7431f874eb)
![image (1)](https://github.com/vkang6378/EC463_miniproject/assets/75413432/b1ef6bca-3e0f-4703-ad1a-6ffe1d941949)
![image (2)](https://github.com/vkang6378/EC463_miniproject/assets/75413432/4d99cd31-1163-4dc8-a97e-c85dcec6664c)




Backend:
The backend was developed using Django and Firebase. It allows users to authenticate using their Google accounts, leveraging Firebase's authentication services. Once authenticated, users can discover other users in the system by fetching a list of all users from a Firestore database. The backend also has messaging functionality, enabling users to send and receive messages. Users can write messages to any other user in the system, and these messages are stored and retrieved from Firestore, ensuring real-time communication capabilities. Below are some of the functions/files that are used for this. 


'google_auth' in 'views.py
This function handles user aythentication using Google accounts. It retrieves an authentication token sent cias POST request. The token is verified using Firebase's 'auth.verify_id_token' method. 

'get_users' function in 'views.py'
This function retrieves a list of users from a Firestore database. It connects to the Firestore client and accesses a collection named "users". All documents in the "users" collection are steamed and converted into a list of dictionaries, each representing a user. A JSON response containing the users' data is returned. 

'send_message' function in 'views.py'
This function handles the sending of messages between users. It collects sender, receiver, and content information form a POST request. It then stores this message data in the "messages" collection in Firestore. A success response is returned after storing the message. 

'simple_mood_analyzer'
This function looks for predefined keywords in the text to determin its mood. More key words or more texting style(such as checking if the text is entirely capitalized etc.) the analyzer can be made more accurate. For instance, if there is a word 'tears' in the text, it can show that the user is sad. 

'settings.py'
This file contains PostgreSQL coniguration, installed apps, middleware, templates, and other setting. 

'urls.py'
This file maps URLs to their corresponding view functions in Django. Each path is associated with a function defined in 'views.py', enabling the handling of specific endpoints like 'google_auth/', 'get_users/', 'send_message/', and 'get_messages/'.












