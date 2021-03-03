+++
title = "2. Demo"
date = 2019-11-18T17:11:28+11:00
weight =5
+++

### Processing a medical document with textract

#### Example
{{< service-example id="textract-example" service="Amazon Textract" inputImage="/images/module-medical-document-processing-and-classification/medical-report-example.png" input="json input" outputImage="/images/module-medical-document-processing-and-classification/medical-report-textract-output.png" test=`This is some <b>HTML</b>,
and a new line with a "quoted string".`>}}

#### How does it work?

1. First we upload our medical document to a predefined S3 bucket.
2. Next we write a script that will run the document analysis against our medical document. 
   
   S3 -> lambda script to kick off document analysis -> on analysis complete -> lambda script to retrieve and process analysis
      
Input
```
textract = boto3.client('textract')
response = textract.start_document_analysis(
    DocumentLocation={
        'S3Object': {
            'Bucket': <bucketName>,
            'Name': <objectName>
        }},
    FeatureTypes=[
        'TABLES',
    ]
    )
```

Output
```

```
### Next Steps
Click [here](../step0/) to setup your notebook.
