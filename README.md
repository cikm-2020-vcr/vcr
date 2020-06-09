# Video Channel Subscription Dataset
This page introcues a newly constructed video channel subscription dataset. The dataset is avaiable at [here](https://drive.google.com/file/d/1cppkO7GqZ2aye8xGII6uEh0hP88-j6VY/view?usp=sharing).

### Description
We collected the data from YouTube which is one of the most popular video media platforms. We collected the channel subscription information of users. The data is collected as follows:


1. In the first step, we choose 10 seed channels that have more than 1M subscribers. Seed channels are selected from a diverse range of categories.

2. Next, we retrieve each channel and selectively collect the videos that have been uploaded to the channels within the previous three months.

3. We then collect a subscription list of users who have commented on the videos.

4. If a channel in the subscription list is not already in the channel set, we add the channel to the channel set.
If there are channels not been retrieved left in the channel set, we repeat steps (2)-(4).

In total, we collect 7,135,931 subscription information from 190,884 users and 1,286,014 channels located in United States. Last, we remove channels that have less than 20 subscribers and users with less than 10 subscriptions. After preprocessing, our new dataset includes **2,148,265 subscriptions** of **106,826 users** and **20,188 channels**. Information of **592,664 videos** including titles, categories, and upload dates are also included in the dataset.

### Statistics
<table style="align=center;">
<tr><td>number of Subscriptions</td><td>2,148,265</td></tr>
<tr><td>number of Users</td><td>106,826</td></tr>
<tr><td>number of Channels</td><td>20,188</td></tr>
<tr><td>number of Videos</td><td>592,664</td></tr>
<tr><td>number of Categories</td><td>16</td></tr>
<tr><td>average number of Subscriptions per User</td><td>20.11</td></tr>
<tr><td>average number of Videos per Channel</td><td>29.36</td></tr>
<tr><td>sparsity</td><td>99.9%</td></tr>
</table>

### Data Format
The data set includes "train.tsv", five "validation_{}.tsv", five "test_{}.txv", "user2id.tsv", "channel2id.tsv", and "video_info.tsv". Each data is represented in the following format:
#### "train.tsv"
```bash
<user_id>\t<channel_id>
```
#### "validation_{}.tsv"
```bash
<user_id>\t<positive_channel>\t<negative_channel_1>\t<negative_channel_2>\t...\t<negative_channel_100>
```
#### "test_{}.tsv"
```bash
<user_id>\t<positive_channel>\t<negative_channel_1>\t<negative_channel_2>\t...\t<negative_channel_100>
```
#### "user2id.tsv"
```bash
<user>\t<user_id>
```
#### "channel2id.tsv"
```bash
<channel>\t<channel_id>
```
#### "video_info.tsv"
```bash
<channel_id>\t<video_id>\t<word_1 word_2 ... >\t<category_id>
```
