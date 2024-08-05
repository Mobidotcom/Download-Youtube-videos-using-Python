import yt_dlp

def download_video(url):
    ydl_opts = {
        'format': 'best',  # Download the best quality video
        'outtmpl': '%(title)s.%(ext)s',  # Save the file with the video title as the name
    }
    with yt_dlp.YoutubeDL(ydl_opts) as ydl:
        info_dict = ydl.extract_info(url, download=True)
        print(f"Title: {info_dict['title']}")
        print(f"Views: {info_dict['view_count']}")
        print("Download complete.")

try:
    url = input("Enter the YouTube URL: ")
    download_video(url)
except Exception as e:
    print("An error occurred:", str(e))
