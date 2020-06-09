# Video Channel Subscription Dataset
This page introcues a newly constructed video channel subscription dataset.

### Description
We collected the data from YouTube which is one of the most popular video media platforms. We collected the channel subscription information of users. The data is collected as follows:


1. In the first step, we choose 10 seed channels that have more than 1M subscribers. Seed channels are selected from a diverse range of categories.

2. Next, we retrieve each channel and selectively collect the videos that have been uploaded to the channels within the previous three months.

3. We then collect a subscription list of users who have commented on the videos.

4. If a channel in the subscription list is not already in the channel set, we add the channel to the channel set.
If there are channels not been retrieved left in the channel set, we repeat steps (2)-(4).

In total, we collect 7,135,931 subscription information from 190,884 users and 1,286,014 channels located in United States. Last, we remove channels that have less than 20 subscribers and users with less than 10 subscriptions. After preprocessing, our new dataset includes **4,129,053 subscriptions** of **77,155 users** and **25,050 channels**. Information of **616,034 videos** including titles, categories, and upload dates are also included in the dataset.

### Statistics
<table style="align=center;">
<tr><td>number of Subscriptions</td><td>2,148,316</td></tr>
<tr><td>number of Users</td><td>106,826</td></tr>
<tr><td>number of Channels</td><td>20,188</td></tr>
<tr><td>number of Videos</td><td>301,309</td></tr>
<tr><td>number of Categories</td><td>15</td></tr>
<tr><td>average number of Subscriptions per User</td><td>20.11</td></tr>
<tr><td>average number of Videos per Channel</td><td>14.93</td></tr>
<tr><td>sparsity</td><td>14.93</td></tr>
</table>

<center>

| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered   |   $12 |
| col 3 is | right-aligned |    $1 |

</center>


### Data Format
