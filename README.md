<h1>🚗 Car Price Prediction Using Machine Learning</h1>

<p>
This project predicts the <strong>selling price of used cars</strong> using machine learning techniques.
It implements a complete <strong>end-to-end ML pipeline</strong> including data preprocessing, feature engineering,
model training, evaluation, and deployment using a <strong>Flask web application</strong>.
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
The project takes raw car data, performs multiple preprocessing steps such as handling missing values,
outlier treatment, categorical encoding, and feature scaling, and trains a regression model to predict
car prices accurately. The trained model is deployed as a web application for real-time predictions.
</p>

<hr>

<h2>📊 Dataset Description</h2>

<h3>Numerical Features</h3>
<ul>
    <li>Year</li>
    <li>Present_Price</li>
    <li>Kms_Driven</li>
    <li>Owner</li>
</ul>

<h3>Categorical Features</h3>
<ul>
    <li>Fuel_Type (Petrol, Diesel, CNG)</li>
    <li>Seller_Type (Individual, Dealer)</li>
    <li>Transmission (Manual, Automatic)</li>
    <li>Brand (Multiple car brands)</li>
</ul>

<hr>

<h2>🔄 Machine Learning Pipeline</h2>

<pre>
Raw Data
   ↓
Missing Value Handling
   ↓
Variable Transformation
   ↓
Outlier Handling
   ↓
Categorical to Numerical Conversion
   ↓
Feature Scaling
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Deployment
</pre>

<hr>

<h2>⚙️ Data Preprocessing Steps</h2>

<h3>1. Missing Value Handling</h3>
<ul>
    <li>Categorical columns are filled using <strong>mode</strong></li>
    <li>Numerical columns are filled using <strong>median</strong></li>
</ul>

<h3>2. Variable Transformation</h3>
<ul>
    <li>Log transformation applied to <code>Kms_Driven</code> to reduce skewness</li>
</ul>

<h3>3. Outlier Handling</h3>
<ul>
    <li>Outliers handled using the <strong>IQR (Interquartile Range)</strong> method</li>
    <li>Extreme values are capped instead of removed</li>
</ul>

<hr>

<h2>🔢 Categorical to Numerical Encoding</h2>

<ul>
    <li><strong>Fuel_Type</strong> → Manual Mapping</li>
    <li><strong>Seller_Type</strong> → Manual Mapping</li>
    <li><strong>Transmission</strong> → Manual Mapping</li>
    <li><strong>Brand</strong> → <strong>Target Encoding</strong></li>
</ul>

<p>
Target Encoding is used for the Brand feature due to its high cardinality.
It reduces dimensionality and improves model generalization.
</p>

<hr>

<h2>📏 Feature Scaling</h2>

<p>
Feature scaling is performed using <strong>StandardScaler</strong>.
</p>

<h3>Scaled Features</h3>
<ul>
    <li>Year</li>
    <li>Present_Price</li>
    <li>Kms_Driven</li>
    <li>Brand (Target Encoded)</li>
</ul>

<p>
Binary categorical features are not scaled to preserve their semantic meaning.
</p>

<hr>

<h2>🤖 Model Training</h2>

<p>
A regression-based machine learning model (<strong>Ridge Regression</strong>) is trained
on the processed dataset to predict car selling prices.
</p>

<hr>

<h2>📈 Model Evaluation</h2>

<ul>
    <li>Evaluation Metric: <strong>R² Score</strong></li>
    <li>Achieved approximately <strong>79% R² score</strong></li>
</ul>

<p>
This performance is consistent with baseline regression models for this dataset.
</p>

<hr>

<h2>🌐 Model Deployment</h2>

<p>
The trained model is deployed using <strong>Flask</strong>.
Users can input car details through a web interface and receive real-time price predictions.
</p>

<h3>Deployment Highlights</h3>
<ul>
    <li>Same preprocessing steps used during training and inference</li>
    <li>Saved artifacts:
        <ul>
            <li>model.pkl</li>
            <li>scaler.pkl</li>
            <li>target_encoder.pkl</li>
        </ul>
    </li>
</ul>

<hr>

<h2>📂 Project Structure</h2>

<pre>
car_price_prediction
│── data/
│   └── car_data.csv
│
│── src/
│   ├── missing_value_handling.py
│   ├── variable_transformation.py
│   ├── outlier_handling.py
│   ├── cat_to_num.py
│   ├── feature_scaling.py
│   └── model_training.py
│
│── models/
│   ├── model.pkl
│   ├── scaler.pkl
│   └── target_encoder.pkl
│
│── templates/
│   └── index.html
│
│── app.py
│── requirements.txt
└── README.md
</pre>

<hr>

<h2>▶️ How to Run the Project</h2>

<h3>1. Clone the Repository</h3>
<pre>
git clone https://github.com/Balavenu123/Car-Price-Prediction.git
cd Car-Price-Prediction
</pre>

<h3>2. Install Dependencies</h3>
<pre>
pip install -r requirements.txt
</pre>

<h3>3. Run the Application</h3>
<pre>
python app.py
</pre>

<p>
Open browser and navigate to:
<code>http://127.0.0.1:5000/</code>
</p>

<hr>

<h2>🛠️ Technologies Used</h2>

<ul>
    <li>Python</li>
    <li>Pandas</li>
    <li>NumPy</li>
    <li>Scikit-learn</li>
    <li>Category Encoders</li>
    <li>Flask</li>
    <li>HTML / CSS</li>
</ul>

<hr>

<h2>📌 Key Learnings</h2>

<ul>
    <li>End-to-end machine learning pipeline design</li>
    <li>Handling high-cardinality categorical features</li>
    <li>Avoiding data leakage</li>
    <li>Model deployment using Flask</li>
</ul>

<hr>

<h2>📄 License</h2>
<p>This project is licensed under the MIT License.</p>
