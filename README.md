# TryHackMe-Upload-vulnerabilities
TryHackMe Upload Vulnerabilities room walkthrough


## Objective:


## Lessons Learned/Skills gained:
- 

## Tools Used:
- Nmap: used


## Walkthrough:

_defence mechanisms used to preven tmalicious fil euploads, and how to circumvent them_

The ways files are filtered are:
  1. Extension Validation
  2. File Type VAlidation
       1. MIME(Multipurpose Internet Mail Extension)
            - format is <type>/<subtype>
      2. Magic Number Validation (HEX header at teh beginning of the file)
           - more accurate but still fakable
           - Editing file with hexeditor
           - A github page lists the magic numbers of GIF
  3. File Length Filtering
  4. File Name Filtering
         - Same name? bad characters htat might cause errors like null bytes, forward salshes on Linux, control chars like ; and unicode chars.
  5. File content filtering

### Bypassing Client Side Fintering
![image](https://github.com/user-attachments/assets/1c6f497e-9b98-4b98-8894-921276c06017)



``accessing shell directly using URI
 - running gobuster revealed a directory named graphics
 - writing hte full URI magic.uploadvulns.thm/graphics/shell.php gave us a reverse shell
### Privilege Escalation  

![image](https://github.com/user-attachments/assets/43a4d2e9-9465-48bd-88bd-b7444ce051b6)


![image](https://github.com/user-attachments/assets/bfff41d5-70ab-42f2-8967-7df8fbbb2d00)


![image](https://github.com/user-attachments/assets/2a362762-3a32-411e-945b-3428cd6c2f25)


![image](https://github.com/user-attachments/assets/9ce73516-c965-4efb-a8e1-0d6ffb36f5a6)
