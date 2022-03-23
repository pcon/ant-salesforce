# ant-salesforce
A collection of ant-salesforce jars for previous versions

# Determining the jar version
## Linux

```bash
unzip -p $file com/sforce/soap/metadata/Connector.java | grep -i END_POINT | \
    grep -i String | awk -F'"' '{print $2}' | rev | cut -d/ -f1 | rev
```