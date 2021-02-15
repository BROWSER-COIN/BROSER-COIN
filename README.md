Skip to content

BROWSER COIN MINER

[(ambas licencias BSD)]

Code
Issues
246
Pull requests
9
Actions
Projects
Wiki
Security
Insights
 3.0.5.0 

https://composer.github.io/installer.sha384sum
luc1an24 Update Plugins.md
…
 1 contributor
75 lines (56 sloc)  3.44 KB
RawBlame
 
Plugins
What is a Plugin?
What is MinerPluginToolkitV1 used for?
List of included plugins
What is a Plugin?
A plugin is an external or internal dependcy (dll). The ABI (Application Binary Interface) is defined in MinerPlugin project and plugin developers must implement the following interfaces IMinerPlugin and IMiner. This means that you create a new project inside Miners directory and implement all required functions from IMinerPlugin and IMiner interfaces. It is recommended that each one is in its own file (Plugin and Miner file).

Each plugin project should implement at least 1 plugin. You can implement more, but good practice is to keep 1 plugin inside 1 project.
IMinerPlugin is used for registering the plugin and there will be only 1 instance created. Its job is to give basic info such as name, UUID, version, etc.
IMiner is the mandatory interface for all miners containing bare minimum functionalities and is being used as miner process instance created by IMinerPlugin.

Bare minimum example of plugin is written in Example Plugin project. The Plugin file contains implementation of IMinerPlugin interface for registration and creation of the plugin instance. The Miner file contains implementation of IMiner interface, providing required functionalities.

What is MinerPluginToolkitV1 used for?
It is recommended to use MinerPluginToolkitV1 as this will enable full integration with Browser mining. It will save time developing it and enable implementation of additional advanced features. If you are writing a plugin we highly recommend that you use MinerPluginToolkitV1. All miner plugins that are developed by Browser miner dev team are using MinerPluginToolkitV1. For example you can check GMiner Plugin.

MinerPluginToolkitV1 also enables creation of Background Services, check out Ethlargement plugin for example.

Advantages	Disadvantages
Implementation of all basic actions like Start/Stop mining, Start benchmarking, retrieve data from API, create command line, etc.

Use of additional features like Configs and Extra Launch Parameters

Access to usefull interfaces providing features like checking for missing files, device cross referencing, initializing internal settings, etc.

The current API is not final and might change in the future.

List of Included Plugins
Miner Plugins
All devices
Xmr-Stak
NVIDIA and AMD
BMiner
ClaymoreDual
GMiner
Phoenix
LolMiner
NanoMiner
NVIDIA
CCMiner
NBMiner
T-Rex
TT-Miner
CryptoDredge
MiniZ
Z-Enemy
AMD
SGMiner
TeamRedMiner
WildRig
CPU
XMRig
Background Services
Ethlargement Pill
© 2020 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
ambas licencias BSD
 
---
items:

 - Yatser/prettypullrequests
 - sanemat/do-not-merge-wip-for-github
 - jasonlong/isometric-contributions
 - ForbesLindesay/github-real-names
 - benbalter/github-mention-highlighter
 - sindresorhus/notifier-for-github
 - OctoLinker/OctoLinker
 - ProLoser/Github-Omnibox
 - Justineo/github-hovercard
 - panzerdp/clipboardy
 - zenorocha/codecopy
 - kamranahmedse/githunt
 - harshjv/github-repo-size
 - sindresorhus/refined-github
 - softvar/enhanced-github
 - bitoiu/markwrap
 - bitoiu/github-red-alert
 - Kibibit/achievibit
 - marpo60/github-compare-tags
 - cheshire137/hubnav
 - ryanflorence/github-plusone-extension
 - Mottie/GitHub-userscripts
 - rgehan/octolenses
 - homerchen19/github-file-icons
 - StylishThemes/GitHub-Dark
 - xthexder/wide-github
 - berzniz/github_pr_tree
 - n1ck/gifs-for-github
 - EnixCoda/Gitako
 - vladgolubev/quickreview-for-github
 - matthizou/github-show-avatars
display_name: GitHub Browser Extensions
created_by: leereilly
---
Some useful and fun browser extensions to personalize your GitHub browser experience.
