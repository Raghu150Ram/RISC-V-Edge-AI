# RISC-V Edge AI Workshop - My Learning Journey

This repository is a documentation of my work from the RISC-V Edge AI Workshop conducted by VLSI System Design.

Through this program, I gained a clear understanding of:

- The implementation and working of machine learning models (Linear Regression, Polynomial Regression, Logistic Regression, KNN, and SVC).
- The implementation and working of deep learning models, specifically Neural Networks (MLP Classifier).
- Using Freedom Studio, interfacing the software with the board, and understanding the basic tools required within the development environment.
- Implementing ML and DL models on a RISC-V platform using Freedom Studio.
- Identifying system limitations and understanding the need for quantization, along with its process.
- End-to-end implementation of quantized models on a RISC-V architecture.

This workshop deepened my understanding of end-to-end edge AI deployment on RISC-V platforms, starting from developing models in Python to quantizing them and implementing them on a RISC-V architecture to reduce RAM usage without compromising model performance.

---
Throughout the 9 days, I progressed through:

- **Day 1:** Introduction to the need for running ML/DL workloads on compact and power-efficient chips. Set up FreedomStudio, executed the SiFive “Welcome” program, reviewed documentation for the VSDQuadron PRO board, and prepared all required files for the workshop environment.
- **Day 2:** Studied foundational ML models, beginning with Linear Regression followed by Polynomial Regression (degrees 2 and 3). Visualized model behavior using Python and Desmos for the 'studentscores.csv' dataset. Trained Linear and Polynomial Regression models on the '50_Startups.csv' dataset as well.
- **Day 3:** Implemented the first machine learning model (Linear Regression) on a RISC-V platform using Freedom Studio. The model was trained on the '50_Startups.csv' dataset and used to predict Profit based on R&D Spend, Administration, and Marketing Spend. Additionally, began working on classification models by implementing Logistic Regression on the 'Social_Network_Ads.csv' dataset and visualized the working of Logistic Regression using Python.

  _***TASK:*** Implemented Polynomial Regression, and implemented Logistic Regression with UART-based inputs._
- **Day 4:** Studied the disadvantages of Logistic Regression and then progressed to implementing the K-Nearest Neighbors (KNN) model using the Social_Network_Ads.csv dataset. After analyzing the limitations of KNN, moved on to implementing the Support Vector Classifier (SVC) on the same dataset.  
- **Day 5:** Imported the coefficient and bias values from Python into a C header file and implemented the SVC model on a RISC-V platform using Freedom Studio to perform output prediction. Additionally, two different prediction functions were implemented to generate the results.

  _***TASK:*** Implemented an 'rbf' based SVC using Freedom Studio using the same dataset._
- **Day 6:** Started with the implementation of an SVC model built on the 'MNIST Kaggle Dataset' (handwritten digit images). This was followed by attempting to deploy the model on a RISC-V platform using Freedom Studio. It was identified that the model could not run on the board due to a RAM overflow issue. Attempts were made to mitigate this by reducing the test dataset size. However, this approach was not successful. As a result, the need for quantization was studied.
- **Day 7:** Quantized all the weights and biases of the models along with appropriate scaling, and implemented the quantized models on a RISC-V platform using Freedom Studio, followed by a complete revision of all the machine learning models developed and learned during the workshop.
- **Day 8:** Introduction to deep learning models, specifically Neural Networks, and their working principles. Built a Neural Network (MLP Classifier) using the MNIST Kaggle dataset.
- **Day 9:** Introduced to the repository developed by Dhanvanti Bhavsar, which was cloned to the local system, and a virtual environment was created to run the programs. The 'training.py' file from the repository was used. Finally, the quantized model was implemented on a RISC-V platform using Freedom Studio, and the input images were successfully classified.

_***TASK:*** Modified the quantization and training parameters accordingly to achieve higher model accuracy._

---
## Acknowledgement

I would like to express my heartfelt thanks to [**Kunal Ghosh**](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/) (VLSI System Design), [**Ankit Mawle**](https://www.linkedin.com/in/ankitmawle/) and [**Dhanvanti Bhavsar**](https://www.linkedin.com/in/dhanvanti-bhavsar-387620160/) for designing and delivering this beautiful course on implementing AI onto RISC-V Architectures.  
Their guidance, enthusiasm, and structured teaching approach made this journey smooth and enjoyable to learn.
