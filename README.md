# downloadXkcd.py

**XKCD Comic Downloader Script**

This Python script, `downloadXkcd.py`, is designed to download every single XKCD comic from the official website. It uses the `requests` library to fetch HTML pages and the `beautifulsoup4` library to parse the HTML content.

**Functionality**

The script works as follows:

1. It starts by setting the initial URL to the XKCD homepage (`https://xkcd.com`).
2. It creates a directory named `xkcd` in the current working directory to store the downloaded comics, using `os.makedirs` with the `exist_ok=True` argument to avoid raising an error if the directory already exists.
3. The script enters an infinite loop, which will continue until it reaches the last comic page (indicated by a URL ending with `#`).
4. In each iteration, it:
	* Downloads the current comic page using `requests.get`.
	* Parses the HTML content using `beautifulsoup