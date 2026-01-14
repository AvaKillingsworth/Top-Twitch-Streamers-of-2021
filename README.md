The first link is the raw data that got from Excel I put into SQL.
The second link is the cleaned data that I took from SQL and put back into Excel. (I forgot my username to PostreSQL lmao)
The third link is the Visualization that I did using Power BI.

Here is also all of my Syntax for SQL:
Who has the most time watched?
SELECT * 
FROM twitchstreamers
ORDER BY total_watch_time DESC
LIMIT 10

Who peaked the most viewers? 
SELECT channel, peak_viewers
FROM twitchstreamers
ORDER BY peak_viewers DESC
LIMIT 10

Who has the highest view count?
SELECT channel, average_viewers
FROM twitchstreamers
ORDER BY average_viewers DESC
LIMIT 10

Who has the most followers?
SELECT channel, total_followers
FROM twitchstreamers
ORDER BY total_followers DESC
LIMIT 10

Who gained the most followers?
SELECT channel, followers_gained
FROM twitchstreamers
ORDER BY followers_gained DESC
LIMIT 10

What is the most spoken language?
SELECT language, COUNT(language)
FROM twitchstreamers
GROUP BY language

What is the partnered ratio?
SELECT partnered, COUNT(partnered)
FROM twitchstreamers
GROUP BY partnered

What is the mature rating ratio?
SELECT mature, COUNT(mature)
FROM twitchstreamers
GROUP BY mature
