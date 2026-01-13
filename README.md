### TFX lab1

TFX was unsucess on macOS. TFX runs successfully only on Linux x86 platforms.

Reference:
https://github.com/raminmohammadi/MLOps/blob/main/Labs/Tensorflow_Labs/TFX_Labs/TFX_Lab1/C2_W2_Lab_2_Feature_Engineering_Pipeline.ipynb
https://www.tensorflow.org/tfx/guide/understanding_tfx_pipelines

In this lab we will
1. Ingest the data using ExampleGen
2. Compute statistics of data using StatisticsGen
3. Infer a schema with SchemaGen
4. Detect anomalies using ExampleValidator
5. Preprocess data into model features suitable for model training with Transform 

Benefits of using tfx transform
- In the backend it uses Apache Beam to transform and preprocess the data. Hence could easily scale for large data
- Creates a transform graph which is frozen graph which can be loaded easily while serving, no need to run code and do recomputation(just run data through the graph and it will be transformed!).
- Run only once! i.e. while training