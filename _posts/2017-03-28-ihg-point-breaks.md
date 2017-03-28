---
layout: post
title: IHG Point Break Hotel Map
---

Most of you reading this probably know what
<a href="https://www.ihg.com/rewardsclub/content/gb/en/redeem-rewards/pointbreaks" target="_blank">IHG point breaks</a> are, but for those who don't, it's when [IHG](https://www.ihg.com/) reduce hotel point redemptions to 5,000 reward points per night in select hotels around the world.

This can mean a saving of over 20,000 points on some hotels per night which is amazing! However, I've always found it quite tricky to spot the hotels I'm interested in when IHG release the (fairly long) list of hotels every few months. So, I decided to create a map of these hotels which will help me, and hopefully some of you, to plan trips. For those interested in the more technical details see below the map.

### The map

Blue Icon = Still up for grabs.
Red Icon = Unavailable.

<iframe src="https://www.google.com/maps/d/embed?mid=1peKGEbnhcfhgjVR8DvVVC60z-74" width="720" height="480"></iframe>

<br/>
If you click the icon on the top left of the map, you can select/deselect which categories you want to see (Remaining/Sold Out). In that pane you can also view a list of the hotels in each category and click on them to bring you to its location. There is also a button to view the map full screen.

I will try and keep this map updated regularly (more often when a new list has been released).

Just because a hotel was available in the current Point Break list, doesn't mean it will be available next time, but it's a good indication what hotels might show up which is why I have included the unavailable hotels on the map too.

### Technical details

I created a Python script to collect the data from IHG, parse it and store it in a suitable format (CSV) to upload to Google Map Maker. The algorithm retrieves the set of all hotels originally announced (A), the set of hotels currently available (B), and finds the relative complement of B in A (A \ B) - which is the unavailable hotels set. It then outputs to two CSV files, one containing the available hotels and the other containing the unavailable ones. Any time an update is required, I can run the script again and upload the output files.

Future improvements include adding the hotel URL to each marker and possibly automating all manual work (although that may be overkill since the data isn't updated _that_ frequently).

<br/>
<br/>
I don't make any money from this website so if you found this map useful feel free to buy me a beer :).

<a href="https://www.paypal.me/CormacQ" target="_blank">PayPal.me</a>
<br/>
<a href="https://monzo.me/cormacquinn" target="_blank">Monzo.me</a>