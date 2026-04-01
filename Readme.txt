Professional Description: Mr. Baig Downloader
Mr. Baig Downloader is a custom-built, graphical desktop application designed to facilitate the downloading of online videos. Developed by Zawar Baig, the tool serves as a user-friendly frontend interface for the powerful yt-dlp command-line utility. It abstracts the complexity of command-line arguments, allowing users to effortlessly fetch, select, and download media in their preferred formats and resolutions.

Core Features
Intelligent URL Parsing: Users can input video links manually or utilize the built-in "Paste" function, which automatically pulls URLs directly from the system clipboard.

Comprehensive Media Fetching: Before downloading, the application retrieves and displays essential video metadata, including the video title and a visual thumbnail, confirming the correct content has been loaded.

Granular Format Selection: The application populates an interactive, scrollable data table (Treeview) detailing all available download formats for the provided URL. The table provides critical information at a glance:

Format ID and File Extension

Resolution (e.g., 1080p, 720p, or "Audio Only")

Quality Details (Video and Audio Codecs)

Estimated File Size

"Best Quality" Automation: For users who want an optimal experience without manually parsing codecs, the tool includes a default "Best Quality" option. This automatically downloads the highest quality video and audio streams and merges them seamlessly.

Real-Time Progress Tracking: Downloads feature a live progress bar and an active status readout that displays the current download percentage, transfer speed (e.g., KiB/s), and estimated time of arrival (ETA).

Customizable Output: Users can easily browse and set their preferred local directory for saved files, defaulting to the standard system Downloads folder.

Technical Architecture
The application is built using Python and leverages several robust libraries and external tools to function seamlessly:

GUI Framework (Tkinter & ttk): The user interface is built using standard Python tkinter combined with ttk (Themed Tkinter) for modern, styled widgets. It uses a clean, custom color palette emphasizing readability with a responsive layout.

Download Engine (yt-dlp): The heavy lifting of extracting media streams from supported websites is handled by the industry-standard yt_dlp library.

Media Processing (FFmpeg): The tool is integrated with ffmpeg.exe to handle post-processing tasks, specifically merging separate high-quality video and audio tracks into a final MP4 container.

Asynchronous Processing (threading): To ensure the graphical interface remains responsive and does not freeze during heavy network operations, both the metadata fetching and the actual downloading processes are offloaded to background daemon threads.

Image Handling (Pillow/PIL): The application uses the Python Imaging Library to dynamically fetch, resize, and render web-based video thumbnails directly into the GUI.

Executable Ready: The codebase includes a resource_path handling mechanism (checking for sys._MEIPASS), indicating it is structured to be easily compiled into a standalone, portable Windows .exe using tools like PyInstaller, bundling its necessary dependencies (like the icon and FFmpeg) directly with the runtime.
