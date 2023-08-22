# TemplateMerger-standalone

This is a JavaScript script that handles the selection, preview, and export of images. The script uses event listeners to detect changes in the file input and clicks on the export button, as well as to detect clicks on two different format options.

When the user selects image files, the handleFileInputChange() function is called. This function clears the preview area and loadedPNGs array, and then loops through the selected files to create a FileReader and read the file as a data URL. Once the file is loaded, a new Image element is created and the loaded image is appended to the preview area. The loaded image is also stored in the loadedPNGs array. Once all images are loaded, the generatePreview() function is called to display a preview of the final image.

When the user clicks on the export button, the handleExportButtonClick() function is called. The function checks the current format option and limits the number of selected files to a certain amount. Then, it generates and displays a preview of the final image. After a short delay to ensure the preview is updated, the function creates a canvas element to hold the combined PNGs and loops through the loaded PNGs to draw them onto the canvas. The function also calculates the position and size of each image based on the format option and number of selected files. Finally, the function converts the canvas to a data URL, creates a Blob from the data URL, creates a download link for the Blob, and simulates a click on the link to trigger the download.

The script also includes a function to convert a data URL to a Blob, which is used in the handleExportButtonClick() function.

Overall, this script provides a user-friendly way to select, preview, and export multiple images in different formats.
