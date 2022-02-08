# Check_GANs
This repo is created to generate synthetic check images. It can generate the whole check images if you have a large dataset size which is shown in the notebook of DCGAN (1). It used the complete check images to generate synthetic check images.
Otherwise, you can train the check-GANs on each component on the check, e.g., logo, signature, handwriting, etc., and assemble them at the end to form the check from the notebook Cifar10-GANs(1). The notebook used Cifar10 as an example to test the structure and then trained deeo neural networks on datasets list below. 


To fulfill the goal of generating different components of check images, multiple datasets have been used to train the check-GANs. The first dataset was selected from bank checks segmentation database (BCSD). This dataset contains 158 images of bank checks with segmentation masks for signatures. It was designed to train a network to extract signatures from bank checks. Each image is 2240px with a resolution of 300px/in. All images were converted to JPEG format. Manual segmentation masks were created for the signatures on these checks, and the dataset was divided into 129 training images and 29 test images. The link of the dataset is list as following: https://www.kaggle.com/saifkhichi96/bank-checks-signatures-segmentation-dataset.


The second dataset was used is signature dataset. CEDAR Signature is a database of off-line signatures for signature verification. Each of 55 individuals contributed 24 signatures thereby creating 1,320 genuine signatures. Some were asked to forge three other writers’ signatures, eight times per subject, thus creating 1,320 forgeries. Each signature was scanned at 300 dpi grayscale and binarized using a gray-scale histogram. Salt pepper noise removal and slant normalization were two steps involved in image preprocessing. The database has 24 genuine and 24 forgeries available for each writer. The link of the dataset is list as following: https://paperswithcode.com/dataset/cedar-signature.

The third dataset was from handwriting recognition. This dataset consists of more than four hundred thousand handwritten names collected through charity projects. Character Recognition utilizes image processing technologies to convert characters on scanned documents into digital forms. It typically performs well in machine-printed fonts. There are 206,799 first names and 207,024 surnames in total. The data was divided into a training set (331,059), testing set (41,382), and validation set (41,382) respectively. The link of the dataset is list below: https://www.kaggle.com/landlord/handwriting-recognition.


The fourth dataset was from logo-2k+ dataset, which is a large-scale logo dataset for scalable logo classification. This real-world logo dataset contains 2,314 categories and 167,140 images. The link of the dataset is listed below: https://github.com/msn199959/Logo-2k-plus-Dataset.



Some results and model structure are shown below along with the check-GANs architecture. 
![generator_plot_500 (1)](https://user-images.githubusercontent.com/62029679/152683304-fb212b96-2b9a-4600-92ec-342d9c5abb7c.png)


![generator_plot_500(32_checks)](https://user-images.githubusercontent.com/62029679/152683310-2eb88f97-15f3-40af-8574-69136ff0c54d.png)


![generator_plot_049](https://user-images.githubusercontent.com/62029679/152683386-1e431459-8e84-4f15-ba02-1c1bdb055b0c.png)


![generator_plot](https://user-images.githubusercontent.com/62029679/152683427-cb0f739d-472a-44c5-b4a5-c4aef30b989b.png)


![discriminator_plot](https://user-images.githubusercontent.com/62029679/152683436-645fadc5-6c72-4da1-8331-272659590fa2.png)


![gan_plot](https://user-images.githubusercontent.com/62029679/152683438-c0b06d31-b673-4a57-a63e-e1a054047d61.png)

