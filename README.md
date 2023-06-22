# YouTube Video and Channel Link Extractor

This Python script scrapes Google search results and extracts video and channel links based on a given query. It utilizes the YouTube Data API to retrieve channel information from video links.

## Intuition

The intuition behind this approach is to use Google search results to find relevant video links based on a query and then extract the associated YouTube channel links. The YouTube Data API is used to retrieve channel information from the video links.

To extract the channel link from a video link, the script follows these steps:
1. If the video URL contains `'?v='`, it extracts the video ID and calls the YouTube API's `videos().list` method to retrieve video details.
2. From the video details response, it extracts the channel ID associated with the video.
3. The YouTube account link is constructed using the channel ID as `https://www.youtube.com/channel/{channel_id}`.

## Execution

To execute the program, follow these steps:

1. Ensure that you have Python 3 installed on your system.
2. Install the necessary dependencies by running the following command:
```
pip install -r requirements.txt
```

3.replace `api_key` in `extractor.py` with your google api key. 
  
4. start program by running the following command:
  
```
python main.py
```

## Optionally you can pass you own url to parse by using the following command:
```
python main.py --query <your_query_String> --num_links <num_of_links_to_retrieve>
```
- `<your_query_string>` should be replaced with the desired search query, e.g., `"site:youtube.com openinapp.co"`.
- `<num_of_links_to_retrieve>` should be replaced with the desired number of video links to retrieve.

