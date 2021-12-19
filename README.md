# DataEngineering-Section-3

Section 3: System Design
You are designing data infrastructure on the cloud for a company whose main business is in processing images.

The company has a web application which collects images uploaded by customers. The company also has a separate web application which provides a stream of images using a Kafka stream. The company’s software engineers have already some code written to process the images. The company would like to save processed images for a minimum of 7 days for archival purposes. Ideally, the company would also want to be able to have some Business Intelligence (BI) on key statistics including number and type of images processed, and by which customers.

Produce a system architecture diagram (e.g. Visio, Powerpoint) using any of the commercial cloud providers' ecosystem to explain your design. Please also indicate clearly if you have made any assumptions at any point.

# Solution Design
Following are the components used in the system design to achieve BI on key statistics of the images uploaded

1. Amazon EC2 to host web application to collect and process images Amazon MSK cluster.
2. Amazon S3 bucket to store the processed data with life cycle policy of 7 days.
3. Amazon EC2 instance to run the Kafka Connect cluster.
4. Amazon EC2 instance to run Lenses for MSK
5. Amazon S3 Bucket  to serve as central metadata repository & Athena to query key statistics
6. Amazon Quick Sight to visualize with BI capability
