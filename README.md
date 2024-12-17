# Charlotte Hornets Active Directory Project

## Description
In this post, I will be detailing how I installed/created two virtual machines (VMs), used Active Directory on one of my VMs to create users/organizational units (OUs)/security groups all pertaining to the Charlotte Hornets. Using these users/OUs/security groups, I was able to create shared files and then map these files for certain users. Lastly, I will showcase how I resolved a hypothetical Help Desk Ticket regarding a user being locked out of their account after too many incorrect passwords. 

This post will be broken down into sections titled VMs Setup, Active Directory, and Help Desk with a Sources section at the very end. I will provide screenshots throughout the Active Directory and Help Desk sections to further illustrate some points. With this preamble out of the way, lets begin with the VMs Setup section.

## VMs Setup
To be upfront and honest, I mimicked Josh Madakor's <a href="https://www.youtube.com/watch?v=MHsI8hJmggI&forced">video</a> to setup my two VMs. I did not follow his steps in regards to running the Powershell script that created roughly 1,000 users since I planned on creating users associated with the Charlotte Hornets Organization. Everything else I essentially followed to a T. I had to recreate this VM multiple times, so I did learn how to do it without the video eventually.

## Active Directory
I cannot find the reddit post I found in regards to how to best learn Active Directory in their opinion, but the person's post detailed how they mimicked their favorite TV show to create users/organizational units/security groups based on the show. This allowed them to learn quite a bit about Active Directory while also keeping the learning entertaining since it related to one of their interests. I absolutely love the Charlotte Hornets (sadly), so I figured why not do an Active Directory inspired project related to them.

I began by looking up people associated with both the Basketball Operations side of the Charlotte Hornets as well as the Business Operations side. This would allow me to create different OUs and security groups to then allow me to have distinct shared files within these groups. I will have my sources down below where I found the staff associated with the business side of the Charlotte Hornets, the coaching staff, the performance staff and the players, but here is a screenshot showcasing the users/OUs/security groups.<br><br>
<img width="500" alt="users-and-groups" src="https://github.com/user-attachments/assets/5db3e9c4-9fbc-4679-9e45-24390cffbb49"><br>
Overall, I ended up having 77 users along with 5 OUs and 5 security groups. Using these security groups, I then created the below shared folders titled Business and Basketball to illustrate the difference between the Basketball and Business Operations.<br>

<img width="500" alt="shared-folders" src="https://github.com/user-attachments/assets/026cb9a9-b950-4fb0-97ed-78bd341cf6e8"><br>

Within both of these shared folders, I was then able to create additional folders to house other information. The screenshot below shows the additional folders I created withinthe Basketball share folder. I had to disable object inheritance for these subfolders in order to get the permissions correct in regards to who could access them. Everyone associated with the Basketball Operations from coaching/performance staff to the players has access to the Basketball shared folder, but everyone does not need access to all of the subfolders. For example, the performance staff and the players have access to the Injuries subfolder meanwhile only the players and the coaching staff have access to the Box Scores subfolder. To further illustrate this point, within the Injuries subfolder are two folders titled "Rehab Programs" and "Injury Reports" of which only players have access to the former while performance staff have access to both. This made my shared folders complicated while I only have 5 Security Groups, I can only imagine what this would be like in an actual corporate environment.<br>

<img width="500" alt="basketball-share" src="https://github.com/user-attachments/assets/fbd68d70-5f3e-46ab-9ad0-cad428492b57"><br>

<img width="500" alt="business-share" src="https://github.com/user-attachments/assets/557a622d-80be-4929-806e-8a2214a8f26e"><br>

<img width="500" alt="scw-mapping-files" src="https://github.com/user-attachments/assets/a1ed5430-837b-4773-8e49-53a437db560b"><br>

<img width="500" alt="scw-mapped-file" src="https://github.com/user-attachments/assets/cce9d657-ca86-46ca-a39f-cc4ebbe2be0c"><br>








## Help Desk
<img width="500" alt="GPO-account-lockout" src="https://github.com/user-attachments/assets/661c4edf-fd21-47e2-88d3-0a64f8551dcf"><br>

<img width="500" alt="LaMelo-locked-out" src="https://github.com/user-attachments/assets/2310ad13-4893-4c03-9fe5-1e8314f45d45"><br>

TICKET IMG GOES HERE

<img width="500" alt="Fixing-LaMelo" src="https://github.com/user-attachments/assets/9d8fb836-c43f-47a0-b128-237e3f958d32"><br>








## Sources
**Josh Madakor's Video**<br>
https://www.youtube.com/watch?v=MHsI8hJmggI&forced<br>
Josh's video helped me setup the domain controller and the windows client VMs.<br>

**KevTech's Active Directory Lab Playlist**<br>
https://www.youtube.com/playlist?list=PLdh13bXVc6-k_u2RPqYAp8R8HtYT_ONht<br>
KevTech's playlist gave me ideas/inspiration to add to my own setup. Overall, his playlists are full of knowledge and are a great way to get some hands on experience with HelpDesk.<br>

**Business/Coaching/Performance Staff along with Players**<br>
https://www.nba.com/hornets/staff (Business Staff)<br>
https://www.nba.com/hornets/news/charlotte-hornets-finalize-2024-25-coaching-staff (Coaching Staff)<br>
https://www.nba.com/hornets/news/charlotte-hornets-announce-2024-25-health-and-performance-staff (Performance Staff)<br>
https://www.spotrac.com/nba/charlotte-hornets/cap/_/year/2024 (Players)<br>
Sites where I found the employees of the Charlotte Hornets Organization.



