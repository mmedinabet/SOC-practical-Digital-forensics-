<h1> Digital Forensics Investigation: Unraveling the Mystery of Gado's Kidnapping </h1>
Our investigation begins with the distressing news that our cat, Gado, has been kidnapped, and the kidnapper has communicated their demands via a Microsoft Word Document. Ransom letter left by the kidnnapper: 

![Screenshot 2024-04-11 2 00 52 PM](https://github.com/mmedinabet/SOC-practical-Digital-forensics-/assets/142737434/71480eaf-93b3-4fe5-ae5c-1fd98d154c1b)

To follow along with the investigation, simply open the terminal on the AttackBox and navigate to the
directory /root/Rooms/introdigitalforensics. This directory contains all the necessary files for our investigation.

![Screenshot 2024-04-11 2 06 49 PM](https://github.com/mmedinabet/SOC-practical-Digital-forensics-/assets/142737434/dd84507c-66d7-4573-8b32-69eaa3f80985)
When you create a text file like TXT, the Operating System stores certain metadata such as the file's creation date and last modification date. However, using advanced editors like MS Word adds more metadata to the file. There are multiple methods to access this metadata, including using official viewer/editors or forensic tools. It's important to note that exporting the file to other formats, such as PDF, usually retains most of the original metadata, depending on the PDF writer used. Let's explore the metadata contained within a PDF file by using the program pdfinfo.

![Screenshot 2024-04-11 4 04 21 PM](https://github.com/mmedinabet/SOC-practical-Digital-forensics-/assets/142737434/52aee927-f76b-4e4f-bea6-17dbda5c92f0)

Utilizing pdfinfo, I was able to find out that the author of the provided PDF file, ransom-letter.pdf is Ann Gree Shepherd.On the other hand, EXIF, short for Exchangeable Image File Format, serves as a standard for storing metadata within image files. When capturing photos with smartphones or digital cameras, a wealth of information becomes embedded in the image. Examples of metadata present in original digital images include details such as the camera or smartphone model, the date and time of image capture, and various photo settings like focal length, aperture, shutter speed, and ISO settings.

Given that smartphones typically feature GPS sensors, it's highly likely to find GPS coordinates embedded in the image. These coordinates, comprising latitude and longitude, typically indicate the location where the photo was taken.

Numerous online and offline tools are available for extracting EXIF data from images. One such tool is exiftool, a command-line utility used for reading and writing metadata across various file types, including JPEG images. In the provided terminal window, we executed the command exiftool IMAGE.jpg to extract all the embedded EXIF data from the image.

![Screenshot 2024-04-11 4 19 49 PM](https://github.com/mmedinabet/SOC-practical-Digital-forensics-/assets/142737434/304a4d1f-84f7-486e-aaba-81937f4fc133)


![Screenshot 2024-04-11 4 24 15 PM](https://github.com/mmedinabet/SOC-practical-Digital-forensics-/assets/142737434/ebb0747e-f729-4ff7-8610-2866168e9f6f)

![Screenshot 2024-04-11 4 27 41 PM](https://github.com/mmedinabet/SOC-practical-Digital-forensics-/assets/142737434/724e6696-5252-41e8-b423-b8bbee028573)


<h2>Conclusion</h2>
In conclusion, this practical exercise highlighted the significant role of digital forensics in investigative processes. It showcased how every action on digital devices leaves behind traces that can be crucial in solving cases. In this scenario, our cat Gado's kidnapping prompted us to analyze a document sent by the kidnapper. By converting the document to PDF format and extracting an image from it, we gained valuable insights into the metadata embedded within these digital artifacts.

Through the use of pdfinfo, we identified key metadata, such as the document's creation details, revealing its origin and creation date. This information provided valuable leads for the investigation. Additionally, the examination of photo EXIF data using tools like exiftool unveiled further details about the image, including the camera model used and GPS coordinates indicating the location where the photo was taken.

By leveraging digital forensic techniques, we were able to gather crucial evidence and insights to aid in the investigation. Ultimately, this exercise demonstrated the importance of digital forensic tools and methodologies in uncovering vital information and unraveling the mysteries behind such incidents.




