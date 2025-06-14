<!-- omit in toc -->
# Stockstir
Easily gather stock data of any company in any of your Python projects

![stockstir-logo](https://github.com/PatzEdi/Stockstir/raw/main/docs/img/stockstir_logo.png)

<p align="center">
	<img src="https://img.shields.io/badge/License-MIT-brightgreen"
		height="23">
	<img src="https://img.shields.io/badge/Creator-PatzEdi-brightgreen"
		height="23">
	<img src="https://readthedocs.org/projects/stockstir/badge/?version=latest"
		height="23">
</p>

<p align = "center">
	<img src="https://static.pepy.tech/badge/stockstir"
		height="23">
	<img src="https://static.pepy.tech/badge/Stockstir/week"
		height="23">
	<img src="https://static.pepy.tech/badge/Stockstir/month"
		height="23">
</p>

<p align = "center">
	<img src="https://img.shields.io/pypi/v/Stockstir?style=flat&color=%23FFA500"
		height="23">
</p>

<!-- omit in toc -->
## Index
- [**Quick Usage**](#quick-usage)
- [**Documentation:**](#documentation)
- [**Changelog**](#changelog)
- [**Features**](#features)
- [**Why?**](#why)
- [**How?**](#how)
- [**User notice**](#user-notice)
- [**Build Instructions**](#build-instructions)
- [**Services used (Credits):**](#services-used-credits)

<br/>
<details>
<summary><strong>Thank you for the support!</strong></summary>
<br/>

**Starrers:**
[@NodeGPTjs](https://github.com/NodeGPTjs), [@waltherg](https://github.com/waltherg), [@anthonyporzio](https://github.com/anthonyporzio), [@mboliveira2006](https://github.com/mboliveira2006), [@JorneVL](https://github.com/JorneVL), [@ddkasa](https://github.com/ddkasa), [@pythoninthegrass](https://github.com/pythoninthegrass), [@jeffcarrico](https://github.com/jeffcarrico), [@kehoecj](https://github.com/kehoecj), [@jftuga](https://github.com/jftuga), [@branislavhesko](https://github.com/branislavhesko), [@drtiwari](https://github.com/drtiwari), [@poa00](https://github.com/poa00), [@gusdanielson](https://github.com/gusdanielson), [@joolybugg](https://github.com/joolybugg), [@BHX2](https://github.com/BHX2), [@electronicjude](https://github.com/electronicjude), [@zdrummond](https://github.com/zdrummond), [@JamesSullivan](https://github.com/JamesSullivan), [@mptsolutions](https://github.com/mptsolutions), [@FrankD412](https://github.com/FrankD412), [@fumbles](https://github.com/fumbles), [@shunsock](https://github.com/shunsock), [@verystealthy](https://github.com/verystealthy), [@agarcialeon](https://github.com/agarcialeon), [@hassan-surmount](https://github.com/hassan-surmount), [@DeflateAwning](https://github.com/DeflateAwning), [@ThinkCode](https://github.com/ThinkCode), [@stvnksslr](https://github.com/stvnksslr),[@rawberg](https://github.com/rawberg), [@z1001123](https://github.com/z1001123), [@soundtrackgeek](https://github.com/soundtrackgeek), [@Giddu](https://github.com/Giddu), [@T31M](https://github.com/T31M), [@somas1](https://github.com/somas1), [@rexzhang](https://github.com/rexzhang), [@arturo-zarzilla](https://github.com/arturo-zarzilla), [@dfd](https://github.com/dfd), [@ArcturusMajere](https://github.com/ArcturusMajere), [@LambertusDekker](https://github.com/LambertusDekker), [@508chris](https://github.com/508chris), [@PandaStacker](https://github.com/PandaStacker), [@piksu](https://github.com/piksu), [@cameronhptdev](https://github.com/cameronhptdev), [@bazfire](https://github.com/bazfire), [@AceofSpades5757](https://github.com/AceofSpades5757), [@georgettica](https://github.com/georgettica), [@LeonardPuettmann](https://github.com/LeonardPuettmann), [@Shrhawk](https://github.com/Shrhawk), [@builderjer](https://github.com/builderjer)

**Thank you for 50+ Stars! Thank you for 35K+ Downloads!**
If you do not wish to be in the list above, please let me know by either creating an issue or messaging me through reddit (linked on my website https://patzedi.github.io). Also, it may take me a while (depending on the time) to put new stargazers on the README, but it will be done nonetheless :) Also, if you are viewing on PyPi, this list above will most likely not be updated to the latest amount of starrers, as I would have to create a new release every time. Commits for new starrers will take place on the GitHub page.

</details>
<br/>
<details>

<summary><strong>A few important notes (Expand to View)</strong></summary>
<br/>

*Verified commits are now being used (Verified commits are used to make sure you know the real developer/trusted person is comitting to the branch/project)*

**Automatic provider integrity/validity checks have now been implemented on my side through crontab! Checks run 5 times a day, and a notification is sent to my phone and desktop to notify me of the status. This way, if any provider fails, I will be notified much sooner than before**

As a reminder, if any errors are found in the documentation, codebase, etc. feel free to create an issue on the Github page. We are all here to learn and improve. Thanks!
</details>

<!-- omit in toc -->
### **Stockstir allows you to reliably gather data of any stock company from any of your Python projects.** 


## **Quick Usage**

Installation:
```
pip3 install Stockstir
```

### Python API Usage

Importing:
```
from stockstir import Stockstir
```
Simple example to gather stock data from any script:
```
price = Stockstir().tools.get_single_price("AMZN") # As an example, we can get the Amazon stock value.

print(price)
```

### Command Line Usage

You can also use Stockstir directly from the command line:
```
stockstir TSLA
```

This will display the current price of Tesla stock in your terminal.

Additional options:
```
stockstir --help                       # Show all available options
stockstir AAPL --provider=insider      # Use a specific provider
stockstir MSFT --random-user-agent     # Use a random user agent for requests
```
<details>
<summary><strong>Stockstir Object Instantiation (Expand to View)</strong></summary>

```
stockstir = Stockstir()
# Below, as an example, we can instantiate the classes within the Stockstir object, which is in this case called stockstir.
tools = stockstir.tools
providers = stockstir.providers
api = stockstir.api
```
You can also customize certain aspects of each Stockstir object you instantiate:
```
stockstir = Stockstir(provider = 'cnbc', random_user_agent=True, print_output = True) # default provider = 'cnbc' (can be set to 'insider' or 'zacks' as well (cnbc recommended)), random_user_agent defaults to False, print_output defaults to False. (Note: print_output is only used for certain funcs such as multi_data_gathering)
# Below, as an example, we can instantiate the classes within the Stockstir object, which is in this case called stockstir.
tools = stockstir.tools
providers = stockstir.providers
api = stockstir.api
```
</details>

<br/>

Since this library has many more features (too many to explain here in a neat way), you can take a look at the [Documentation](https://stockstir.readthedocs.io/en/latest/index.html) hosted by readthedocs.io.

## **Documentation:**
Access the [Stockstir ReadtheDocs Documentation](https://stockstir.readthedocs.io/en/latest/index.html) to explore the features of Stockstir and how to use them, as well as getting to know how Stockstir works in a detailed way. The documentation is now updated to the latest version.

## **Changelog**
- Latest Version: ![PyPI - Version](https://img.shields.io/pypi/v/Stockstir?style=flat-square&color=%23000)
- [Changelog](/CHANGELOG.md) (Start Date : December 30, 2023)

## **Features**
- A complete fail-safe system with three providers (Read documentation for more information on *providers*).
- Gather stock data of any company using cnbc, insiders, or zacks as the current providers (alternative to yfinance)
- Includes a single price gathering tool to get the price of any company once.
- Includes a multi data gathering tool which has features like anti ban, random user agents, delay for each request, and of course how much data to gather.  
- Get the trend of the gathered data determining whether the stock price went up, down, or stayed neutral throughout that time period.
- Ability to return the time spent in the total process of gathering the data. This can be useful in order to analyze data and comparing it to the time spent overall. Not only that, but getting the trend also comes with an optional option to get the change between the first and the last value of the gathered data.
- Includes a tool to create logs of the data gathered if needed, and does so by writing the data to a file at a specified directory of your choice.
- Includes the ability to make requests with random user agents (up to 24 different agents).
- Parameter customization of Stockstir objects (more information in the documentation).
- Command line interface (CLI) for quick stock price lookups directly from your terminal.
- Error handling in case of wrong inputs.
- Many more features listed in the documentation.
## **Why?**
- As an alternative to other systems like yfinance, Stockstir insures that you can always gather stock company data no matter what. It is a simple way to gather stock data without the need to learn full-fledged systems.
- Real time stock data can be used to look at a specific price of any company and determine what to do with that data later on. For example, if you wanted to get notified once the price of stock goes above or below a value, it is a simple task to do something like that. 

## **How?**
- Stockstir mainly works by sending a request to *providers* (view documentation for more information), and parsing the request via a regex pattern to gather the price. It currently has three providers with a fail-safe mechanism that switches provider if the selected one fails. (Again, view documentation to learn more about providers and their functionality).

## **User notice**
- Please be aware that using a rotating IP address (for example a VPN with a rotating IP) could help you not get banned from a provider when making a lot of requests. If you want to use the multi data gathering tool, you can use the anti ban function to try to avoid getting banned from the website and being recognized as a potential "bot" making automatic requests.
- This project is still a work in progress. Adding new features is very easy, but so far I have started with it simple. 
- Please note that the README file briefly goes into the details of how the project works. If you want more in depth details of what each and every function and parameter does, take a look at the [Documentation](https://stockstir.readthedocs.io/en/latest/index.html) hosted on readthedocs.io.
- Also, I am not responsible for any inappropriate use of this library, such as being used for spam or mass-collection purposes. This project is strictly for educational purposes only.

## **Build Instructions**
To build Stockstir directly onto your local machine without installing from pypi, you can follow these steps below:
1. Clone the repository:
```
git clone https://github.com/PatzEdi/Stockstir
```
2. Enter the project files directory (assuming you are in the same directory as when you cloned Stockstir):
```
cd Stockstir
```
3. Build and install Stockstir via pip3:
```
pip3 install -e .
```
4. Done! Stockstir is now installed on your local machine.

## **Services used (Credits):**
- [Requests module](https://requests.readthedocs.io/en/latest/)
- [URLLib module](https://docs.python.org/3/library/urllib.html)
- [Re module](https://docs.python.org/3/library/re.html)
- [Time module](https://docs.python.org/3/library/time.html)
- [Random module](https://docs.python.org/3/library/random.html)
<details>
<summary><strong>Contributors (Expand to View)</strong></summary>
Thank you all for your suggestions for improving Stockstir!

<br/>

1. [striata](https://www.reddit.com/user/striata/) for the suggestions on following PEP guidelines and code efficiency enhancements in [this post](https://www.reddit.com/r/Python/comments/18uuyjr/comment/kfnju1d/?utm_source=share&utm_medium=web2x&context=3), thank you!

2. [PandaStacker](https://github.com/PandaStacker) for taking the time to suggest new functions for Stockstir in [this pull request](https://github.com/PatzEdi/Stockstir/pull/3). Thanks for the contributions!

3. [suvanbanerjee](https://github.com/suvanbanerjee) in [pull request #8](https://github.com/PatzEdi/Stockstir/pull/8) for adding new error handling to the api class. Thanks!

*Contributors in this list gave me permission to put them on the README*
</details>

<!-- omit in toc -->
## **Many Thanks**
- Thank you for your interest in Stockstir. If you like this project, please leave a star :)

[^ Back to top ^](#stockstir)
