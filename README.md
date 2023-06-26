# MWF-Dataset
In this project, we introduce a malicious webshell family dataset, called MWF dataset. Malicious webshells currently present tremendous threats to cloud security. And fine-grained multi-classification is urgently needed to enable precise responses and active defenses on malicious webshell threats. This dataset contains 1,359 malicious webshell samples originally obtained from the cloud servers of Alibaba Cloud. Each of them is provided with a family label. The samples of the same family generally present similar characteristics or behaviors. The dataset has a total of 78 families and 22 outliers. It has potential in cloud security and generalized sequence, graph, and tree data analytics and visualization.

# Supporting information
- MWF Dataset:  
For each sample, a CSV metadata file is provided to present the dynamic function calls captured by running the sample in a sandbox. The file name uses the uuid and file md5 (i.e., uuid_filemd5) of the sample to indicate the server ID where the sample is found and its file md5. In the file, each record represents a function call with five single-valued attributes and a multi-valued attribute. The single-valued attributes include the call index, caller, callee, argc, and return value of a function call. The multi-valued attribute is the argv of the callee in the function call. The values of this multi-valued attribute are formatted in an array of length n, where n is equal to the argc. Each element in the argv array is recorded as the form of [parameter index, formal parameter, actual parameter].

- Ground truth of the MWF dataset.
The ground truth of the MWF dataser is provided in a CSV file named “BasicInfo” in Table 1, each record in this file has two fields, namely, the uuid_filemd5 and family_id of a sample. The uuid_filemd5 acts as unique identifier for locating the metadata file of the sample. The family_id uses an integer to indicate a sample’s family. Samples sharing the same family_id belong to the same malicious webshell family. Notably,a “-1” family_id value indicates that the corresponding sample is an outlier.


