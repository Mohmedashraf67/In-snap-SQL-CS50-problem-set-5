Problem and Solution Overview
Problem to Solve
With the evolution of communication methods from the printing press to the postal service, telegrams, and now messaging apps, speed has become a critical factor. Modern messaging apps like Facebook Messenger, iMessage, Instagram, Signal, and Snapchat rely on near-instant communication. A delay of even a few milliseconds can result in a missed connection.

I was tasked with writing SQL queries for a fictional app similar to Snapchat, where users can send pictures that expire 30 seconds after being viewed by the recipient. The goal was to ensure the app's core features were implemented correctly and efficiently, as thousands of users depend on the app for instant communication. My queries needed to be not only correct but also optimized for speed, making use of indexes to enhance performance.

How I Used My Database Skills to Solve It
To address the challenges faced by the app's owner, I implemented the following SQL solutions:

Identifying Active Users:

Problem: The app's user engagement team needed to find all usernames of users who logged in since 2024-01-01.
Solution: I wrote a query to fetch these usernames using the search_users_by_last_login index for efficient retrieval.
Preventing Re-opening of Expired Messages:

Problem: Users needed to be prevented from re-opening messages that have expired.
Solution: I crafted a query to find the expiration time of a specific message (ID 151) using the primary key index for quick lookup.
Ranking Best Friends:

Problem: The app needed to rank a user’s “best friends” based on message frequency, similar to Snapchat’s “Friend Emojis” feature.
Solution: I developed a query to identify the top 3 users to whom creativewisdom377 sent messages most frequently, utilizing the search_messages_by_from_user_id index to optimize the query.
Finding the Most Popular User:

Problem: The app required a summary of user engagement to identify the most popular user based on the number of messages received.
Solution: I wrote a query to determine the username of the most popular user, leveraging the search_messages_by_to_user_id index to enhance performance.
Listing Mutual Friends:

Problem: The app needed to quickly show a list of mutual friends between two users.
Solution: I created a query to find the user IDs of mutual friends between lovelytrust487 and exceptionalinspiration482, making use of the sqlite_autoindex_friends_1 index for efficient results.
Conclusion
By writing these optimized SQL queries and ensuring they made use of the appropriate indexes, I was able to help the app owner implement crucial features that allowed users to communicate swiftly and reliably. This not only solved their immediate problems but also contributed to a smoother, more responsive user experience.
