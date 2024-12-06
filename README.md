<p align="center">
  <img src=https://github.com/limwelwel/PICTURES-AND-GIF/blob/45690003adbaf80745de882b8ec46f450184efbc/midterm%20electives/1.png alt=Bsu style="height: 150px;">
  <hr>
<h3 align="center">COLLEGE OF ENGINEERING</h3>
<h3 align="center">BACHELOR OF SCIENCE IN MECHATRONICS ENGINEERING</h3>
<h3 align="center">MeXE 402 - Mechatronics Engineering Elective 2: Data Science and Machine Learning: Finals: Pair-Based Project</h3>
<h1 align="center"> OpenCV Projects </h1> 
<br> 

## I. Introduction
<p align="justify"> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Adding text to images is a fundamental task in computer vision, serving as a bridge between visual and textual information. It plays a crucial role in numerous applications, including image annotation, visual communication, and augmented reality. The challenge lies in placing text that is both visually appealing and contextually informative while considering factors such as text positioning, font style, size, color, and the background's complexity. The ability to overlay text on images enables effective data representation, enhances interpretability, and facilitates tasks such as automated labeling, dynamic content generation, and accessibility improvements. In computer vision, this capability is essential for creating informative datasets, developing human-computer interaction systems, and enriching real-world visual understanding. By addressing challenges such as text readability, positioning, and seamless integration with diverse image contexts, the task highlights the significance of combining visual and textual data for smarter and more intuitive visual systems.

## II. Abstract
<p align="justify"> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This project aims to develop an efficient and flexible system for adding text to images, addressing the challenges of text readability, aesthetic integration, and dynamic adaptability to varying image contexts. The approach involves leveraging OpenCV for precise text placement, customization of font styles, sizes, and colors, and handling diverse image backgrounds to ensure clarity and visual appeal. By automating text overlay processes, the system is expected to enhance applications in image annotation, watermarking, and data visualization. The outcome of the project will be a robust tool that improves the utility and interpretability of images in computer vision tasks, making it a valuable asset for research, education, and industry.

## III. Project Methods
- **Import Libraries**:
     - Prepare the environment by importing necessary libraries.
          - Use the cv2 library for image processing (reading, writing, editing images).
          - Import cv2_imshow from Google Colab to display images (since cv2.imshow doesn't work in Colab).

- **Load Image**:
     - Specify the image path (e.g., image_path = '/content/image.jpg').
     - Load the image using cv2.imread(image_path) to make it editable.

- **Define Text Details**:
     - Create a list of dictionaries for player information. Each dictionary includes:
          - **Name**: Player's name (e.g., "Dwight Ramos").
          - **Jersey Number**: Player's jersey number (e.g., "Jersey No. 24").
          - **Position**: Coordinates for placing text on the image (e.g., (x, y)).
     - This dynamic structure supports adding text for multiple players.

- **Set Font Properties**:
     - Define the appearance of the text:
          - **Font Style**: Use cv2.FONT_HERSHEY_SIMPLEX, cv2.FONT_HERSHEY_DUPLEX, or similar.
          - **Font Size**: Set the font scale (e.g., 1.0).
          - **Thickness**: Adjust for legibility.
          - **Text Color**: Define in BGR format (e.g., (0, 0, 0) for black).
     - Adjust properties for better visibility against the background.

- **Add Text to Image**:
     - Loop through the player details and overlay text:
          - Use cv2.putText to add the player's name and jersey number.
          - Apply positions and font properties dynamically from the dictionary.
     - Optionally, enhance design:
          - Use colors inspired by the Philippine flag (e.g., red, yellow, blue).
          - Alternate colors for names and jersey numbers for visual appeal.

- **Display Modified Image**:
     - Use cv2_imshow(image) to display the edited image in Google Colab.
     - Verify the placement and styling of the text.
     
## IV. Conclusion
<p align="justify"> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The project successfully demonstrated the use of OpenCV to overlay player details, such as names and jersey numbers, onto an image. This was achieved with customizable text properties, including font style, size, color, and positioning, ensuring clarity and readability. The use of thematic colors inspired by the Philippine flag added a creative and visually appealing element to the output.

<p align="justify"> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; However, several challenges were encountered during the process. Ensuring the text remained legible against complex or busy backgrounds required careful selection of text colors and placement. Adjusting positions dynamically for multiple players to avoid overlap or misalignment also presented a difficulty, especially when dealing with varying image layouts. Managing color contrast was crucial to maintaining visibility without compromising the aesthetic quality of the annotations.

<p align="justify"> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Despite these challenges, the outcomes were highly positive. The final annotated images were clear, organized, and visually appealing, effectively highlighting player details. The methodology developed is not only reusable but also scalable, making it applicable for similar image annotation tasks in sports, presentations, or other creative projects. This work emphasizes the balance between technical precision and design considerations in image processing.

## V. Additional Materials

<p align="justify"> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This program demonstrates the process of adding a player's name and jersey number to an image of a Gilas Pilipinas basketball player using OpenCV. The code is designed to enhance the visual appeal of the image while clearly displaying the player's information.
  
### Code for Adding Player Name and Jersey Number to one Gilas Pilipinas Basketball Player Image

    import cv2
    from google.colab.patches import cv2_imshow

    # Load the uploaded image
      image_path = '/content/Gilas Pilipinas Basketball/gilas jb.jpg'
      image = cv2.imread(image_path)
    
    # Get the image dimensions
      image_height, image_width, _ = image.shape
    
    # Define text details for the single player
      player = {"name": "Justin Brownlee", "number": "Jersey No. 32", "position": (100, 400)}  # Adjusted Y-position for a lower placement
    
    # Font properties
      font = cv2.FONT_HERSHEY_TRIPLEX
      font_scale = 4.5  # Increased the font scale for better visibility
      font_color = (0, 0, 0)  # Black
      thickness = 5  # Increased thickness for better visibility
    
    # Add text to the image for the single player
      name_text = player["name"]
      number_text = player["number"]
      x, y = player["position"]
    
    # Add name
      cv2.putText(image, name_text, (x, y), font, font_scale, font_color, thickness, lineType=cv2.LINE_AA)
    # Add jersey number (slightly below the name)
      cv2.putText(image, number_text, (x, y + 200), font, font_scale, font_color, thickness, lineType=cv2.LINE_AA)
    
    # Resize the image for display (adjust width and height as needed)
      output_width = 600  # Set desired width
      output_height = int(image_height * (output_width / image_width))  # Keep aspect ratio
      resized_image = cv2.resize(image, (output_width, output_height))
    
    # Display the resized image
      cv2_imshow(resized_image)
    
    # Save the modified image
      output_path = '/mnt/data/gilas_single_player_with_text.jpg'
      cv2.imwrite(output_path, resized_image)
      print(f"Image saved to {output_path}")

### Code for Adding Players Name and Jersey Numbers to three Gilas Pilipinas Basketball Players Image

    import cv2
    from google.colab.patches import cv2_imshow
    
    # Load the uploaded image
      image_path = '/content/Gilas Pilipinas Basketball/Gilas Pilipinas.jpg'
      image = cv2.imread(image_path)
    
    # Get the image dimensions
      image_height, image_width, _ = image.shape
    
    # Define text details for each player
      players = [
          {"name": "Dwight Ramos", "number": "Jersey No. 24", "position": (50, 50)},  # Left player
          {"name": "Kai Sotto", "number": "Jersey No. 11", "position": (540, 50)},    # Middle player
          {"name": "Justin Brownlee", "number": "Jersey No. 32", "position": (1300, 50)}, # Right player
      ]
      
    # Font properties
      font = cv2.FONT_HERSHEY_DUPLEX
      font_scale = 1.3
      thickness = 2
    
    # Define the colors based on the Philippine flag (Blue, Red, Yellow)
      colors = [(0, 0, 255), (0, 255, 255), (255, 0, 0)]  # Red, Yellow, Blue (BGR format)
    
    # Add text to the image with flag-based colors
      for i, player in enumerate(players):
          name_text = player["name"]
          number_text = player["number"]
          x, y = player["position"]
    
        # Use a different color for each player (cycling through the flag's colors)
          name_color = colors[i % len(colors)]
          number_color = colors[(i + 1) % len(colors)]
    
        # Add name with the selected color
          cv2.putText(image, name_text, (x, y), font, font_scale, name_color, thickness, lineType=cv2.LINE_AA)
    
        # Add jersey number slightly below the name with another color
          cv2.putText(image, number_text, (x, y + 40), font, font_scale, number_color, thickness, lineType=cv2.LINE_AA)
    
    # Resize the image for display (adjust width and height as needed)
      output_width = 800  # Set desired width
      output_height = int(image_height * (output_width / image_width))  # Keep aspect ratio
      resized_image = cv2.resize(image, (output_width, output_height))
    
    # Display the resized image
      cv2_imshow(resized_image)
    
    # Save the modified image
      output_path = '/mnt/data/gilas_with_flag_text.jpg'
      cv2.imwrite(output_path, image)
      print(f"Image saved to {output_path}")

### Results
<p align="center">
<img src="Images/gilas jb.png"  height="500px"/> <img src="Images/gilas dwight.png" height="500px"/> <img src="Images/gilas kai.png" height="500px"/>

<p align="center">
<img src="Images/gilas pilipinas.png"  height="500px"/>

## VI. References
Misbah Mohammed. (2020, December 29). OpenCV Tutorial - Easy run on Colab with Code [Video]. YouTube. https://www.youtube.com/watch?v=E3Lg4aZVCAU

In photos: Gilas Pilipinas 11 for FIBA OQT. (n.d.). One-network. https://www.onesports.ph/gilas/article/22284/in-photos-gilas-pilipinas-11-for-fiba-oqt#google_vignette






<hr>
<p align="center">
  <img src=https://github.com/limwelwel/PICTURES-AND-GIF/blob/45690003adbaf80745de882b8ec46f450184efbc/midterm%20electives/2.png alt=Bsu style="height: 25px;">
