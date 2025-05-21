## Objective
The aim of this endeavor is to develop a sophisticated waste segregation framework leveraging convolutional neural networks (CNNs) to effectively differentiate and classify waste into discrete categories. This initiative aspires to bolster recycling efficacy, mitigate ecological degradation, and foster environmentally sustainable waste management protocols.
## The key goals are:

* Precisely categorising waste materials into distinct classifications such as cardboard, glass, paper, and plastic. 
* Enhancing the efficiency of waste segregation to facilitate recycling processes and curtail landfill contributions. 
* Gaining deeper insights into the characteristics of various waste materials to refine sorting strategies and advance sustainability efforts.

## Data Description
* The dataset is organized into several folders, each corresponding to a specific category, such as Cardboard, Food_Waste, and Metal. • Each folder contains images of objects that fall within its respective classification.
* However, the items within these folders are not further distinguished into subcategories. For example, the Food_Waste folder may include images of items like coffee grounds, teabags, and fruit peels, but these are not explicitly labeled as coffee grounds or teabags.However, these items are not further subcategorised.

### 📊 *Findings About the Data*

1. *Class Distribution*:

   * The dataset contains *7 classes*: Cardboard, Food_Waste, Glass, Metal, Other, Paper, and Plastic.
   * Some classes, like Plastic (459 samples), have significantly *more examples* than others like Cardboard (108 samples).
   * This class imbalance can lead to biased model performance (e.g., higher recall for Plastic).

2. *Image Sizes*:

   * Images were resized to *128×128 pixels* for consistency, ensuring uniform input shape for the model.

3. *Label Encoding*:

   * Labels were *one-hot encoded*, making them compatible with categorical classification using softmax.

---

### 🤖 *Model Training Summary*

1. *Architecture*:

   * 3 Convolutional Layers (with ReLU, BatchNorm, MaxPooling)
   * Fully connected dense layers with Dropout to prevent overfitting
   * Softmax layer for multiclass classification

2. *Training Setup*:

   * Optimizer: *Adam*
   * Loss Function: *Categorical Crossentropy*
   * Batch Size: *32*
   * Epochs: *20*
   * Input Shape: *(128, 128, 3)*
   * Total Parameters: Moderate (good balance of complexity vs. speed)

3. *Performance on Validation Set*:

| Metric    | Value      |
| --------- | ---------- |
| Accuracy  | *61.84%* |
| Precision | 62.12%     |
| Recall    | 61.84%     |
| F1 Score  | 61.07%     |

4. *Class-wise Performance*:

   * Plastic: Highest recall (0.79), likely due to class having more data.
   * Glass and Other: Lower recall & F1-score, likely due to fewer examples or similar features to other classes.
   * Cardboard, Food_Waste, and Metal perform reasonably well.
  
## Data Augmentation
- Create a Data Augmentation Pipeline
- Train and Evaluate the model on the new augmented dataset
  
## Conclusions (Major)

| Metric    | Value      |
| --------- | ---------- |
| Accuracy  | *61.84%* |
| Precision | 62.12%     |
| Recall    | 61.84%     |
| F1 Score  | 61.07%     |


