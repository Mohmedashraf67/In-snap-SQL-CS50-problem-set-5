
    <h1>Snap Messaging App SQL Queries</h1>

    <h2>Overview</h2>
    <p>This repository contains SQL queries designed for a fictional messaging app that allows users to send pictures which expire 30 seconds after the recipient views them, inspired by Snapchat. The goal of these queries is to implement core features efficiently, ensuring fast and reliable communication for thousands of users.</p>

    <h2>Problem to Solve</h2>
    <p>With the evolution of communication methods from the printing press to the postal service, telegrams, and now messaging apps, speed has become a critical factor. Modern messaging apps like Facebook Messenger, iMessage, Instagram, Signal, and Snapchat rely on near-instant communication. A delay of even a few milliseconds can result in a missed connection.</p>
    <p>I was tasked with writing SQL queries for a fictional app similar to Snapchat, where users can send pictures that expire 30 seconds after being viewed by the recipient. The goal was to ensure the app's core features were implemented correctly and efficiently, as thousands of users depend on the app for instant communication. My queries needed to be not only correct but also optimized for speed, making use of indexes to enhance performance.</p>

    <h2>How I Used My Database Skills to Solve It</h2>
    <p>To address the challenges faced by the app's owner, I implemented the following SQL solutions:</p>

    <h3>Identifying Active Users</h3>
    <p><strong>Problem:</strong> The app's user engagement team needed to find all usernames of users who logged in since 2024-01-01.<br>
    <strong>Solution:</strong> I wrote a query to fetch these usernames using the <code>search_users_by_last_login</code> index for efficient retrieval.</p>

    <h3>Preventing Re-opening of Expired Messages</h3>
    <p><strong>Problem:</strong> Users needed to be prevented from re-opening messages that have expired.<br>
    <strong>Solution:</strong> I crafted a query to find the expiration time of a specific message (ID 151) using the primary key index for quick lookup.</p>

    <h3>Ranking Best Friends</h3>
    <p><strong>Problem:</strong> The app needed to rank a user’s “best friends” based on message frequency, similar to Snapchat’s “Friend Emojis” feature.<br>
    <strong>Solution:</strong> I developed a query to identify the top 3 users to whom <code>creativewisdom377</code> sent messages most frequently, utilizing the <code>search_messages_by_from_user_id</code> index to optimize the query.</p>

    <h3>Finding the Most Popular User</h3>
    <p><strong>Problem:</strong> The app required a summary of user engagement to identify the most popular user based on the number of messages received.<br>
    <strong>Solution:</strong> I wrote a query to determine the username of the most popular user, leveraging the <code>search_messages_by_to_user_id</code> index to enhance performance.</p>

    <h3>Listing Mutual Friends</h3>
    <p><strong>Problem:</strong> The app needed to quickly show a list of mutual friends between two users.<br>
    <strong>Solution:</strong> I created a query to find the user IDs of mutual friends between <code>lovelytrust487</code> and <code>exceptionalinspiration482</code>, making use of the <code>sqlite_autoindex_friends_1</code> index for efficient results.</p>

    <h2>Conclusion</h2>
    <p>By writing these optimized SQL queries and ensuring they made use of the appropriate indexes, I was able to help the app owner implement crucial features that allowed users to communicate swiftly and reliably. This not only solved their immediate problems but also contributed to a smoother, more responsive user experience.</p>

