# Breast-Cancer-Detection

<h2>Purpose</h2>
        <p>The purpose of this project is to detect breast cancer from CT scans 
            using image segmentation. I built two models in both PyTorch and Tensorflow
        using UNETs of different architectures.</p>
        <div class="images">
            <div class="image">
                <img src="images/breast-cancer-tf.png" alt="">
                <p>TensorFlow Model</p>
            </div>

            <div class="image">
                <img src="images/breast-cancer-torch.png" alt="">
                <p>PyTorch Model</p>
            </div>
            
        </div>
        

        <h2>Methodology</h2>
        <p>One UNET was built in Tensorflow and Keras, the architecture contains 2 - 3x3 
            convolutional layers per block and uses 5 blocks on both the contracting and 
        expanding path to get the image into a latent space with dimension 256. The model also
        used a batc size of 32 and trained for 10 epochs. 
        Using BCE Dice loss the model achieved 0.9 validation accuracy.<br><br>
        The other UNET was built in PyTorch, I experimented with many loss funcitons including
        dice, BCE dice, BCE, focal loss and Tversky loss. I also tuned the model with hyperparameter
        grids to achieve higher accuracy. The optimized model ended up brinign the image to 1024 dimensions
        in latent space before the expanding path. The best loss function was binary cross entropy which resulted
        in roughly 0.4 dice loss during testing. <br><br>

        Both models used Adam or AdamW in training and used reduce learning on plateau 
        for the LR scheduler. 

        <h2>Techniques</h2>
        <ul class="tech">
            <li>
                <h3>Biomedical Image Segmentation</h3>
            </li>
            <li>
                <h3>TensorFlow</h3>
            </li>
            <li>
                <h3>Keras</h3>
            </li>
            <li>
                <h3>PyTorch</h3>
            </li>
            <li>
                <h3>Numpy</h3>
            </li>
            <li>
                <h3>UNET</h3>
            </li>

        </ul>
