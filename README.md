
# YouTube Video and Channel Link Extractor

This Python script scrapes Google search results and extracts video and channel links based on a given query. It utilizes the YouTube Data API to retrieve channel information from video links.

## Intuition

The intuition behind this approach is to use Google search results to find relevant video links based on a query and then extract the associated YouTube channel links. The YouTube Data API is used to retrieve channel information from the video links.

To extract the channel link from a video link, the script follows these steps:
1. If the video URL contains `'?v='`, it extracts the video ID and calls the YouTube API's `videos().list` method to retrieve video details.
2. From the video details response, it extracts the channel ID associated with the video.
3. The YouTube account link is constructed using the channel ID as `https://www.youtube.com/channel/{channel_id}`.



