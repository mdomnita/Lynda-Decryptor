# Video2Brain (Lynda-Decryptor) with subtitle conversion

You may have noticed that if you want to download Videos from Video2Brain, the only way is to use the Video2Brain desktop app.
Now you can use this application to decrypt all videos and create a folder structure with normal titles instead of hash values.

## Usage
- Please download the latest binary from release section ([download](http://lyndadecryptor.tk/LyndaDecryptor.zip))

- Extract the files with your favorite compression tool or built in os functions.
- Open commandline and navigate to the extracted folder containing LyndaDecryptor.exe
- Execute LyndaDecryptor.exe with LyndaDecryptor /F [PathToEncryptedFile] [PathToDecryptedFile] or LyndaDecrytor /D [FolderWithEncryptedFiles] where you have to replace the "PathToEncryptedFile", "PathToDecryptedFile" or "FolderWithEncryptedFiles" with the relative or full path to your files.

There are some flags you can use to control the behavior:
- /RM will remove encrypted files after decryption
- /OUT is available to specify an output folder for decrypted files
- /DB [PATH] let you specify the full path to the database containing titles (to get rid of these odd names)

Example command with database used to name the files correctly (Windows 10):
LyndaDecryptor.exe /D "<courses_directory>\<course_number>" /DB "c:\Users\<username>\AppData\Local\Lynda.com\Lynda.com Desktop App\db.sqlite"

Subtitles are converted and renamed automatically with the SubtitleConvertor I built with help from @rosetinted
Converting subtitles is possible (thanks to @mdomnita) with this little tool [Repo](https://github.com/mdomnita/LyndaCaptionToSrtConvertor)

---

## Limitations
This program is **windows only** at the time of this writing. You can compile it under Linux and Mac using [Mono](http://www.mono-project.com/) or [DotNetCore](https://www.microsoft.com/net/core), with some changes due to the sqlite platform binding.

At the moment **decrypting files from android or ios apps are not supported**

---

![Lynda.com](https://upload.wikimedia.org/wikipedia/en/b/b1/Official-company-logo-for-lynda.com_400x400px.png)
