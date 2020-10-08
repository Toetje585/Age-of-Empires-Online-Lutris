# Age-of-Empires-Online-Lutris

Runs Age of Empires Online on Lutris (Linux)

THIS IS WORK IN PROGRESS

Runs Age of Empires Online (Project Celeste) using DXVK (Vulkan) on Linux using the Lutris - Open Gaming Platform.

# Requirements:

Sadly due the launcher not working in Wine due .NET Framework you will need a fully patched game from following https://www.projectceleste.com/install/.

Documentation is limited for now.

Install  the wrapper by using:

lutris -i ~/path_to_script/aoeo_celeste.json

Afterwards copy the patched game to:

/Games/age-of-empires-online/drive_c/Program Files/Age of Empires Online

Edit the launch agruments in Lutris:

--email ""
--password ""
--online-ip "" (Lan co-op only, not needed in most casses)
