# TopSinhalaMP3 Downloader
Song downloader for [TopSinhalaMP3](https://www.topsinhalamp3.com/) and [NewSinhalaMP3](https://www.newsinhalamp3.com/). 
This program able to download MP3s for particular artist or even all the artist at one go.
Need `python3` with `bs4`, `urllib` and `shutil` to work. Works in any OS with python3 support.
These requirements are been taken care of in the installation process. 

## Installation

For installation on the machine:

```bash
  $ git clone https://github.com/randikabanura/top_sinhala_mp3_downloader
  $ cd top_sinhala_mp3_downloader
  $ python setup.py install
```

For one time use:

```bash
  $ git clone https://github.com/randikabanura/top_sinhala_mp3_downloader
  $ cd top_sinhala_mp3_downloader
  $ python topsinhalamp3/main.py
```

## Usage

On the start you will be select the mode you want to operate. This will give ability to download
all songs or select artist to download songs for that artist. Selection will be look like following:

```bash
Do you need to search by:
        1) Artist Letter 
        2) Artist Name 
        3) All Artists
        4) Top 25 by Month 
        5) All Top 25 by Month 
        6) New by Month 
        7) All New by Month
```

After selecting the desired option please follow the on screen details to download songs.
Also, you can change the configurations in the `topsinhalamp3/downloader/consts.py` file to customize the downloading process.
Please DO NOT change anything except of the following options.

```bash
file_download_path = './downloads' # Can change download location for the files
update_mp3_tag = True # If you make this false mp3 tags will not be updated.
database_enabled = False # This need to have the mysql database with same schema provided in ./db folder
force_downloadable = True # Download and replace even if file already exists
cover_art_generation = True # Generate cover art for song (inspiration from Spotify)
cover_art_only_album = True # Use album name instead of song name for cover arts
cover_art_delete_after_attached = True # Delete cover arts after image has been attached to mp3

# If you want to upload songs to s3 bucket please configure following options
enabled_s3_upload = True
keep_local_file_after_download = False
bucket_name = 'media'  # Bucket must be available
bucket_endpoint = '' # Can use AWS S3, DigitalOcean spaces, Wasabi S3 and other S3 compatible services
access_key = ''  # Need to have write access
secret_access_key = '' # Need to have write access
```

## Developer

Name: [Banura Randika Perera](https://github.com/randikabanura) <br/>
Linkedin: [randika-banura](https://www.linkedin.com/in/randika-banura/) <br/>
Email: [randika.banura@gamil.com](mailto:randika.banura@gamil.com) <br/>
Bsc (Hons) Information Technology specialized in Software Engineering (SLIIT) <br/>

Name: [W. Kalansooriya](https://github.com/bhanudv) <br/>
Email: [chandrabhanudv@gmail.com](mailto:chandrabhanudv@gmail.com)
