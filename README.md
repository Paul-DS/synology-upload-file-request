# Bash script to upload a file to a Synology NAS using a file request

This method can be used to upload files from an external device, without allowing the device to access any NAS data (no read/list rights).

Tested on DSM7.

## Dependencies

This script requires to have `bash` and `curl` installed.

## Download

Clone the repository:

`git clone https://github.com/Paul-DS/synology-upload-file-request.git`

Or download the script directly:

`wget https://raw.githubusercontent.com/Paul-DS/synology-upload-file-request/main/synology-upload-file-request.sh`

Or:

`curl -O https://raw.githubusercontent.com/Paul-DS/synology-upload-file-request/main/synology-upload-file-request.sh`

## Usage

`bash synology-upload-file-request.sh --host [HOST] --sharing_id [SHARING_ID] --password [PASSWORD] --uploader_name [UPLOADER_NAME] --file [FILE_TO_UPLOAD]`

### Options

|Parameter|Required|Description|
|---|---|---|
|-H,  --host|Required|Host name of the Synology NAS, including the protocol (HTTP/HTTPS) and the port, without trailing slash<br />Examples: `http://192.168.0.123:5000`, `https://www.example.com:1234`|
|-S, --sharing_id|Required|Sharing ID provided by Synology.<br />Example: if the URL provided is `https://www.example.com/sharing/abcdef12`, the Sharing ID would be `abcdef12`|
|-P, --password|Optional|The password for the file request, if defined|
|-F, --file|Required|The file to upload|
|-U, --uploader_name|Required|Uploader name|