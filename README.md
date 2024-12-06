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

## IV. Conclusion


## V. Additional Materials


## VI. References





<hr>
<p align="center">
  <img src=https://github.com/limwelwel/PICTURES-AND-GIF/blob/45690003adbaf80745de882b8ec46f450184efbc/midterm%20electives/2.png alt=Bsu style="height: 25px;">
