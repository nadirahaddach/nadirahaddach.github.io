{% include navigation.html %}
# Create Task Outline
### Idea: RGB Student Art Feature
_Description:_ Rgb with grayscale feature that dynamically changes RGB values. In the process of making pinkscale feature.
<br>
### [Overview of the CB “Create Performance Task”](https://apcentral.collegeboard.org/pdf/ap-csp-student-task-directions.pdf?course=ap-computer-science-principles)
- Final program code (created independently or collaboratively)
- A video that displays the running of your program and demonstrates functionality you developed (created independently)
- Written responses to all the prompts in the performance task (created independently)
- Scoring guidelines and instructions for submitting your dry run performance task are the same as those on the AP Computer Science Principles Exam page on AP Central.  The differences: document code, answers, and place Video link on Wiki/Jekyll Page; incorporate code into your PBL project.
_Final Program Code Requirements:_
- Instructions for input from one of the following:
- - the user (including user actions that trigger events)
- - **Example:** in [rgb.html](https://github.com/Tyler929/WalkieTalkies/blob/main/templates/rgb.html) (button that toggles grayscale and regular image by user input)
```
img class=“img-responsive py-3" id=img{{loop.index}} alt=“” width=“256" height=“Auto” src=“{{image.base64}}“>
                            <p hidden id=“img_orig{{loop.index}}“>{{image.base64}}</p>
                            <button onclick=“toggle()“>Grayscale!</button>
```
```
var imageType = 2;
        function toggle() {
            if (imageType == 2) {
                $(‘#colorscale’).hide()
                $(‘#grayscale’).show()
                imageType = 1; <!-- allows for toggling back and forth -->
            } else {
                $(‘#grayscale’).hide()
                $(‘#colorscale’).show()
                imageType = 2; <!-- allows for toggling back and forth -->
            }
        }
```
<br>

- Use of at least one list (or other collection type) to represent a collection of
data that is stored and used to manage program complexity and help fulfill
the program’s purpose
- - **Example:** in [image.py](https://github.com/Tyler929/WalkieTalkies/blob/main/image.py)
```
def image_data(path=Path(“static/rgb/“), img_list=None):  # info: path of static images is defaulted
    if img_list is None:  # info: color_dict is defined with defaults and these are the images showing up
        img_list = [
            {‘source’: “Ceramics 2”, ‘label’: “Nadira Haddach”, ‘file’: “lassen-volcano-256.jpg”},
        ]
```
<br>

- At least one procedure that contributes to the program’s intended purpose,
where you have defined:
- - the procedure’s name
- - the return type (if necessary)
- - one or more parameters
- - **Example:**
```
return img_list  # list is returned with all the attributes for each image dictionary
```
```
var imageType = 2;
        function toggle() {
            if (imageType == 2) {
                $(‘#colorscale’).hide()
                $(‘#grayscale’).show()
                imageType = 1; <!-- allows for toggling back and forth -->
            } else {
                $(‘#grayscale’).hide()
                $(‘#colorscale’).show()
                imageType = 2; <!-- allows for toggling back and forth -->
            }
        }
```
<br>

- An algorithm that includes sequencing, selection, and iteration that is in the
body of the selected procedure
- - **Example:**
```
 img_dict[‘hex_array_GRAY’] = []
        img_dict[‘binary_array_GRAY’] = []
        # for grayscale binary/hex changes
        for pixel in img_dict[‘gray_data’]:
            # hexadecimal conversions
            hex_value = hex(pixel[0])[-2:] + hex(pixel[1])[-2:] + hex(pixel[2])[-2:]
            hex_value = hex_value.replace(“x”, “0")
            img_dict[‘hex_array_GRAY’].append(“#” + hex_value)
            # binary conversions
            bin_value = bin(pixel[0])[2:].zfill(8) + ” ” + bin(pixel[1])[2:].zfill(8) + ” ” + bin(pixel[2])[2:].zfill(8)
            img_dict[‘binary_array_GRAY’].append(bin_value)
```
<br>

- Calls to your student-developed procedure
- - **Example:**
```
img class=“img-responsive py-3” id=img{{loop.index}} alt=“” width=“256” height=“Auto” src=“{{image.base64}}“>
                            <p hidden id=“img_orig{{loop.index}}“>{{image.base64}}</p>
                            <button onclick=“toggle()“>Grayscale!</button>
```
<br>

**Written Responses:**
<br>
3a) The overall purpose of this program is to give students an opportunity to display artwork in a fun and creative way. Students will be able to display their art in different color schemes, giving a different perspective on the work. It could also be part of an activity to create art and then greyscale it to get a final result. The functionality shown in the video is the user clicking the greyscale button turning the image grey as well as the user clicking the bluescale button which changes the photo to blue. Also, the artwork displays the name of the creator. The video demonstrates inputs and outputs. The input demonstrated here is the user clicking the button, being the input, and the image changing colors, being the output. 
<br>
3b)
```
def image_data(path=Path(“static/rgb/“), img_list=None):  # info: path of static images is defaulted
    if img_list is None:  # info: color_dict is defined with defaults and these are the images showing up
        img_list = [
            {‘source’: “Ceramics 2”, ‘label’: “Nadira Haddach”, ‘file’: “lassen-volcano-256.jpg"},
        ]
```
```
  for img_dict in img_list:
        # to fix static images
        file = path / img_dict['file']
        print(file)

        img_reference = Image.open(file)
        img_data = img_reference.getdata()  # https://www.geeksforgeeks.org/python-pil-image-getdata/
        img_dict['format'] = img_reference.format
        img_dict['mode'] = img_reference.mode
        img_dict['size'] = img_reference.size

        # info: Conversion of original Image to Base64, a string format that serves HTML nicely
        img_dict['base64'] = image_formatter(img_reference, img_dict['format'])

        # info: Numpy is used to allow easy access to data of image, python list
        img_dict['data'] = numpy.array(img_data)
        img_dict['hex_array'] = []
        img_dict['binary_array'] = []
        # grayscale
        img_dict['gray_data'] = []
```
The name of the list being used in this code segment is "img_list". The data in the list represents the image file displayed on the page. The list also consists of the source/label of the image, which is metadata about the image. The list manages complexity in my program by preventing repetition of the code segment for each reference. Without the list, the code would be much more confusing and unorganized. Each time the image was mentioned in the code, all of the list would have to be repeated, creating more room for error and making debugging a lot more difficult. 
<br>

3c)
```
if len(pixel) > 3:
                # grayscale
                img_dict['gray_data'].append((average, average, average, pixel[3]))
            else:
                # grayscale
                img_dict['gray_data'].append((average, average, average))
```
```
<div>
                                <button type="button" id=myImage onclick="changeImage()">Color/Greyscale</button>
                            </div>
```
The identified procedure contributes to the program by giving the function of the page. The greyscale button is one of the main functionalities on the page, it gives the page purpose as without it the page would simply be html. The procedure allows users to change their image to different scales of color. The identified procedure works with backend python code from image.py, this code consists of averaging the data of each pixel of an image to create a grayscale image. This function is then called by the click of a button to switch the image to greyscale and back. 
<br>
d)
```
<div>
                                <button type="button" id=myImage onclick="changeImage()">Color/Greyscale</button>
                            </div>
```
```
 <p hidden id="img_orig{{loop.index}}">{{image.base64}}</p>
                            <p hidden id="img_gray{{loop.index}}">{{image.base64_GRAY}}</p>
```
The condition tested by the first call is if the button is clicked and the image is normal, the image will be changed to grayscale. On the other hand, the condition on the second call is if the image is already greyscale, the image will be reverted to the original. The result of the first call is the image changing to greyscale whereas the result of the second call would be the image changing to normal. 
