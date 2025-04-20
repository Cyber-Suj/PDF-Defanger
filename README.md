# PDF Defanger

PDF Defanger is a open-source collection of shell scripts and configuration files that automatically sets up a Postfix mail server with advanced PDF filtering. All PDF files received will be rendered in a sandbox before applying OCR and recompiling the output into a new, safe PDF file. This makes any PDF file safe to view even if the original file was malicious. This is intended to allow users to *safely* receive and view PDFs sent over email without having to change their workflow.
This software runs on Linux and uses a combination of Postfix, MIMEDefang, Apptainer, MuPDF, and Tesseract to achieve its goal.


## Installation

Copy all files to a directory

```wget https://github.com/Cyber-Suj/PDF-Defanger/archive/refs/heads/main.zip```

Extract the files

```unzip -j main.zip```

Make autoSetup.sh executable

```chmod +x autoSetup.sh```

Specify a package manager and run autoSetup.sh

```./autoSetup.sh dnf```

Currently supported package managers are apt and dnf.

Note: When installing on Debian-based distributions a popup will ask how to configure Postfix, and what domain name to use. If you are just testing out PDF Defanger's basic functionality, you should pick the 'Local only' configuration and use a domain name such as 'localhost.localdomain'. This will allow test emails to be sent locally through PDF Defanger.

### List of Tested Distributions
PDF Defang has been tested, and successfully ran on the following distributions:
- CentOS Stream 9
- Fedora 41 Workstation
- Ubuntu 24