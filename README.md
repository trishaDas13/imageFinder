# imageFinder

##hoisting Link: https://trishadas13.github.io/imageFinder/

#HTML code description: 
Heading ("h1"Image Search App"/h1"):

A level 1 ("h1") heading displaying "Image Search App." This likely serves as the main title of the web page.
Search Bar ("div class="searchBar""):

A "div" element with the class "searchBar" containing a search input field and a search button.
The input field has a placeholder text that reads "Search for images...."
The button is labeled "Search" and is used to initiate the image search.
Image Display ("div class="images"""/div"):

A "div" element with the class "images." This is likely intended to display the search results, which may include images.
Loading Message ("div class="loading""):

A "div" element with the class "loading" that displays the message "Loading images ...." to indicate to the user that images are being loaded.
Dialog for Image Display ("dialog"):

A "dialog" element that is likely used for displaying images in a modal or dialog-like format.
Inside the dialog, there's an "img" element with an empty src attribute, which can be used to display images when a user clicks on a search result.
#CSS code description: 
Universal Reset: The code begins with a universal reset, setting margin, padding, and box-sizing to ensure consistent styling across elements.

Body Styles: The body element is set to occupy the full viewport width and height. It's organized as a flex container with elements vertically centered. The overflow-x property is hidden to prevent horizontal scrolling.

Heading Styles: h1 elements are centered with text-align and have a margin of 2rem.

Search Bar Styles: The .searchBar class styles a search bar section. It's a flex container with wrapped content (flex-wrap) and centers content both horizontally and vertically. It has a maximum width, padding, and a subtle box-shadow.

Input Styles: The input elements within the search bar are styled with padding, border-radius, font size, background color, border properties, box-shadow, and no outline (removing the default input focus outline).

Button Styles: The button elements within the search bar have background color, border-radius, text color, a cursor pointer, and other styles. On hover, the opacity of the button changes.

Image Results Styles: The .images class styles a grid for displaying image results. It uses CSS Grid (grid-template-columns) to create a responsive layout with three columns and a gap between images. Images have padding and border-radius.

Loading Indicator Styles: The .loading class is used to hide a loading indicator (the display property is set to "none"). This class can be used to show or hide a loading animation as needed.

Media Queries: There are media queries for responsiveness. When the screen width is below 768px, the grid changes to two columns, and when the screen width is below 425px, it changes to a single column. This makes the layout more user-friendly on smaller screens.
#Javascript code description: 
It selects various elements on the web page and stores them in variables:

btn: Represents a button element used to trigger the image search.
input: Represents an input element where the user enters the search query.
images: Represents an element where the fetched images will be displayed.
loading: Represents an element that is displayed during the loading process.
It adds an event listener to the button (btn) to handle the image search when the button is clicked.

When the button is clicked, the code does the following:

Clears the contents of the images element by setting its innerHTML to an empty string.
Retrieves the user's search query from the input element and stores it in the search variable.
Displays the loading element by setting its style.display to 'flex', making it visible.
It sets a timeout using setTimeout to simulate a loading delay:

Inside the timeout function, it makes an asynchronous request to the Unsplash API using the fetch function.
The API request URL includes the search query provided by the user and an Unsplash client ID for authentication.
It waits for the API response and stores the JSON data in the res variable.
It then processes the API response (res) by iterating through the images in the results property of the response object:

For each image, it creates a new div element and appends it to the images element.
Inside each div, it adds an img element with the src attribute set to the full URL of the image from the API (elem.urls.full).
It also adds an alt attribute to the img element with the value "Error," and a link (a element) to the Unsplash photo page of the image.
It appends the div to the images element, effectively displaying the image in the web page.
After all the images have been processed and added to the images element, it hides the loading element by setting its style.display to 'none', indicating that the loading process is complete.

#Summary:
In summary, this code allows users to search for images on Unsplash using a search query entered into an input field. After searching, the images matching the query are displayed on the web page, and a loading indicator is shown while the images are fetched from the Unsplash API.
