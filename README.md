# Requirements

You must install `BeautifulSoup` from pip

`pip install BeautifulSoup` 

# How to use

In the Configuration block, you'll want to correctly set the `SITE_URL` to your domain. If you have an XSL file, you'll include that in the same folder as this script, otherwise, you can ignore it. 

The search directory will search for your files to convert into an RSS feed. It accepts relative paths, along with absolutes.

Then, in `Add basic channel info`, you'll want to edit it for your title and description as you need them to be. There is also the ability to set your favicon as the thumbnail if you have one. 

The code block 

`                    subdirectory = None
                    if "../port/" in file_path:
                        subdirectory = "port"
                    elif "../tut/" in file_path:
                        subdirectory = "tut"
                    elif "../blog/" in file_path:
                        subdirectory = "blog"`
						

Is honestly pretty rough, and there's probably a cleaner way of it. You're setting your subdirectory in here, as shown above as the example, otherwise, the code won't parse the subdirectory. Set the `subdirectory` as the name of the dir.

# What is processed_files?

It's an automated way of verifying that when you have an RSS update, it won't re-send all the older ones, and will only create new RSS feeds for new stuff. Neat :-)

## What are the features?

It has favicon and thumbnail support. The thumbnail is pulled from the first image scene by default. It's compliant with w3 standards. It doesn't display the text in the RSS reader, just the description, but most readers have the option to display the full text anyway.
