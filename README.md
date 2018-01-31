# dq-packer-data-pipeline


# Additional install notes

Progress DataDirect ODBC connector for GP needs manual install after the base AMI has been created using the extracted file already copied to the machine.
Go to C:\tmp\install\PROGRESS_DATADIRECT_CONNECT64_ODBC_7.1.4_WIN_64\setup.exe and run the installer manually. Use the answers from C:\tmp\install\response.properties

Pseudo Ansible would look like the following however it does not work at present.

- name: Install Progress Datadirect
  win_command: cmd /C C:\tmp\install\PROGRESS_DATADIRECT_CONNECT64_ODBC_7.1.4_WIN_64\setup.exe -f C:\tmp\install\response.properties –i silent
