The aim of this project is how to use face as an authentication system for an attendance system.

face_recognition is an ai model that scans and recognize human faces, cv2 is opencv-python package, csv will be used for manipulating data in csv file, 
os to handle files and folders

Videocapture is a method of opencv that takes input (here source is 0 or default webcam).

load_image_file is used to load images face_encodings will create encoded data for that image that face_recognition package will use for performing 
operations, we have 4 faces in our example to recognize, known_face_encoding is the list of encoding of all the 4 faces , known_faces_names is name of all
of them students is a copy of know faces that we will use mark the attendance (basically we will remove names that are present), face_locations, face_encodings,
ace_names are empty lists for input image (we will compare with specific recognized face for recognition), current time is current time (as the name suggests) 
we will use this for accurate attendance, f is the variable having all the data of current date csv file and we are opening it with write mode, lnwriter is 
write variable on f.
we will create a infinite loop and store the incoming frame into frame variable , a new small frame variable is created to store resized image and the
scale of decrement is 0.25% on both x and y rgb_small_variable will store the rgb equivalent of the small frame, we need thisas face_recognition
package used rgb format ,face_locations and face_encodings variables will store the face encoding and locations of incoming frames.
we will create a for loop to iterate on face_encoding values andinside for looop we will compare incoming encoding and locations
with know ones and if its present we will recognise what is the name of that face (for more detailed explanation watch the video) after that we will
append that name into face_names list and display a text on the video output with name , font is saved in fonts variable , and opencv will use putText to
actually put that text.
if the name is present in students list remove it from there as the student is marked as present once , current time is updated in the csv using date time
package , the final task is to display the user video stream and also a exit condition which in this case is press of button ‘q’,
after this the only thing left is to release the video capture (close video input stream) destroy all opened windows and close the opened file.
