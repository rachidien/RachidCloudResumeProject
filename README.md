# RachidCloudResumeProject
This is an html/css project for Google Cloud Academy with BambooGeeks

The guide is based on this Google Cloud lab : "Google Cloud Essential Skills: Challenge Lab"
Link : https://www.cloudskillsboost.google/focuses/1734?parent=catalog.

------------------------------

Step by step guide for installing a webserver via SSH , and uploading website files

------------------------------
1 - Create the linux VM : enabling http port (80) for the web server

2 - Access the VM using ssh

3 - Install a webserver (apache in our case) with the command :
   
	 sudo apt-get install apache2
	 
4 - Test the webserver using external IP of the VM (access via a browser).

5 - Uploading the project files to a bucket named "rachidtata". The files are in the folder "My-Resume-cloud-project".

6 - Copy the files from the bucket to the webserver "/var/www/html/" directory. The files are hosted in a temporary bucket "rachidtata". I used: "gsutil cp" cammand.

sudo gsutil cp -r gs://rachidtata/My-Resume-cloud-project/index.html .
sudo gsutil cp -r gs://rachidtata/My-Resume-cloud-project/my_cv.jpg .
sudo gsutil cp -r gs://rachidtata/My-Resume-cloud-project/mystyle.css .

6 - Re-Test of the webserver using external IP of the VM (access via a browser). (You can remove the files and the bucket).





