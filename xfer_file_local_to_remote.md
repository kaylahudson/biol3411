# How to Transfer Files from Local to Remote (or Vice Versa)
1. Open your terminal.
2. Identify the path of your local file.
3. Use `scp` to transfer your local file to a remote server: `scp <local_file_path> <destination_server>`
  1. Note: you may have to enter a password if your local and/or remote servers have restricted access
4. Navigate to the remote server and verify that the file has been transferred!
