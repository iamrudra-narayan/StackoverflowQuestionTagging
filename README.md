# Stackoverflow Question Tagging (InstructorEmbedding + ANN)

Find the complete code, dataset and Reference by <b><a href="https://drive.google.com/drive/folders/19fKEdJLikmDe6p7nbcfMBzYsejW5tvJF?usp=sharing">CLICKING HERE</a></b>

<img src="https://www.codespot.org/assets/other/stack-overflow.jpg">
<br>
<h2><b>INTRODUCTION</b></h2>
<br>
<ul>
  <li>In the expansive landscape of programming, developers worldwide rely on platforms like Stack Overflow for insights, solutions, and collaboration. With its vast repository of questions spanning diverse topics, Stack Overflow serves as a cornerstone of support for the developer community. However, as the volume of questions continues to grow, manual tagging becomes increasingly burdensome and prone to errors.</li>

<li>To address this challenge, we delve into the realm of machine learning to automate the tagging process on Stack Overflow questions. Our goal is to develop a predictive model capable of suggesting relevant tags for new inquiries, enhancing searchability and user experience. Through this notebook, we embark on a journey to explore data preprocessing, feature engineering, model selection, and evaluation, ultimately aiming to empower developers with an efficient and accurate tagging system. Join us as we harness the power of machine learning to enrich knowledge sharing and collaboration within the Stack Overflow community.</li>
</ul>
<br>
<br>
<h2><b>ABOUT DATASET</b></h2>
<h4><b>Download the Dataset by  <a href="https://www.kaggle.com/code/miljan/predicting-tags-for-stackoverflow/input"><b>CLICKING HERE</b></a></b></h4>
<br>
<ol>
  <li><strong>Question Dataset (question.csv):</strong>
   <ul>
     <li>Columns: 'Id', 'OwnerUserId', 'CreationDate', 'ClosedDate', 'Score', 'Title', 'Body'</li>
   </ul>
</li>

<li><strong>Answer Dataset (answer.csv):</strong>
   <ul>
     <li>Columns: 'Id', 'OwnerUserId', 'CreationDate', 'ParentId', 'Score', 'Body'</li>
   </ul>
</li>

<li><strong>Tags Dataset (tags.csv):</strong>
   <ul>
     <li>Columns: 'Id', 'Tag'</li>
   </ul>
</li>
</ol>
<ul>
    <li><strong>QuestionId:</strong> A unique identifier for each question on Stack Overflow.</li>
    <li><strong>OwnerUserId:</strong> The user ID of the individual who posted the question.</li>
    <li><strong>CreationDate:</strong> The timestamp indicating when the question was posted.</li>
    <li><strong>ParentId:</strong> For answers, this column references the ID of the question being answered.</li>
    <li><strong>Score:</strong> The score assigned to the question or answer by community members, reflecting its quality or relevance.</li>
    <li><strong>Title:</strong> The title of the question, providing a concise overview of its content.</li>
    <li><strong>Body:</strong> The body of the question, containing detailed information and context.</li>
    <li><strong>Tag:</strong> The tag(s) associated with the question, providing categorization and aiding in searchability.</li>
  </ul>
<br>
<br>
<h2><b>Approaches For Feature Engineering</b></h2>
<br>
<ul>
    <li><strong>Data Selection:</strong> You selected important features from three datasets: Id, Title, Body, and Tags.</li>
    <li><strong>Data Sampling:</strong> You randomly sampled 100,000 datapoints from the selected features.</li>
    <li><strong>Text Preprocessing:</strong> You cleaned and preprocessed the Title and Body columns, likely including steps such as tokenization and lowercasing.</li>
    <li><strong>Word Embedding:</strong> You converted the preprocessed text data into vector arrays using pre-trained word embeddings, specifically using an embedding with a dimension of 768.</li>
    <li><strong>Tag Filtering:</strong> You filtered tags based on their frequency, keeping only those tags that occur more than 50 times in the dataset.</li>
    <li><strong>Multi-label Binarization:</strong> You used a MultiLabelBinarizer to convert the selected tags into a binary matrix representation suitable for multi-label classification, resulting in 262 unique tags.</li>
</ul>
<br>
<br>
<h2><b>CONCLUSION</b></h2>
<br>
<ul>
  <li>
    In conclusion, this notebook presents the development of a predictive model for automating tag prediction on Stack Overflow questions. Leveraging machine learning techniques and a comprehensive dataset comprising question and tag information, we have demonstrated the potential for enhancing searchability and user experience on the platform. Through rigorous experimentation and evaluation, we have established the effectiveness of our model in accurately predicting tags for new questions based on their titles and bodies. Moving forward, the integration of this model into the Stack Overflow platform could streamline question classification and improve searchability, ultimately fostering knowledge sharing and collaboration within the developer community.
  </li>
</ul>
<br>
<br>
<h2><b>REFERENCES</b></h2>
<br>
<ol>
    <li><b>Stackoverflow Overview:</b> https://www.kaggle.com/code/miljan/predicting-tags-for-stackoverflow/notebook</li>
    <li><b>Research paper:</b> https://arxiv.org/pdf/2212.09741</li>
    <li><b>Instruction Embedding Implementation:</b> </li>
        <ul>
          <li>https://pypi.org/project/InstructorEmbedding/</li>
          <li>https://github.com/xlang-ai/instructor-embedding</li>
        </ul>
  <li><b>Instruction Embedding Blog:</b> https://instructor-embedding.github.io</li>
</ol>
<br>
<br>
<h1><b>THANK YOU</b></h1>
