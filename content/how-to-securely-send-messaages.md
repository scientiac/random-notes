+++
title = "How to Securely send Messages"
date = 2025-03-03T22:26:27+05:45
[taxonomies]
tags = ["understanding"]
+++

[_Here, letterbox is the box that contains the letter not the letterbox of your home, where the
postman puts the letter._]

First you buy(make) a ton of locks that can be locked without a key but can't
be unlocked without your key. [_There should only be one key that unlocks the lock
and only you should have it._] Then, you distribute your locks everywhere where
your friends who send you important messages live, [_distribute them in public, they're just locks that
only your key can open._] maybe send a bag or two of those locks to them.

When sending you a letter ask your friend to quickly lock their letter in a box [_becomes letterbox_] with
their own lock+key that both locks and unlocks the box for convenience.
Then ask them to lock __their key__ that they used to lock the letter box (letterbox-key) __using the
lock you have given__, whenever they are sending you a letter.
[_The message is secured._]

Now tell them to parcel the letter [_That is locked using their key
and their key is locked with your key_] in any way they
want because no one except you can unlock that box since only you have the key
to unlock the box to get their key that they used to lock the letter. [_You get two boxes,
a box that contains the letter, __and__ another box that contains the key of your friend
to open the letterbox secured by your lock._]

To open the letter you open the lock of the box that contains the letterbox-key using your key.
Then you open the letterbox using the letterbox-key. [_then you throw the letterbox lock+key that your
friend used because it's only needed once -- like a disposable lock._] And enjoy the letter.

[_Your friend locked the letter with his own lock+key first because it is easier for them
to lock the letter with their own key, and it's simpler to lock that small key
with the lock you've given._]

This is how PGP works. In summary:

1. You distribute your public "lock" to everyone.
2. Your friend uses a temporary lock (symmetric key) to secure their message in a box.
3. They then secure the key for that temporary lock by locking it with your public lock
   (asymmetric encryption).
4. Only you have the key (private key) to open that envelope and retrieve the temporary
   key, which then allows you to unlock the box and see the message.

[_And that's how we send encrypted emails._]
