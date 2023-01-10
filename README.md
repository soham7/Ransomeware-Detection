# Ransomeware-Detection
I have trained an extremely small amount of samples based on dataset from https://github.com/manabu-hirano/RanSAP and trained it on a random forrest model with oob score of 0.66.
The scope of this project is to apply the same model to ransomware families like Lockfile (which relies of intermittent encryption, hence making the documents partially readable. The problem with this kind of encryption is that it does not require a lot of input/output (I/O) disk operations and does not communicate with a command and control server, which makes it much harder to spot and allows for encrypting files without internet access & letting system write file ie making it a system process.) and find how effective it is able to detect.

For extracting the I/O stream I need to setup a thin visor(waybackvisor) since it would provide a stream undisturbed from OS interruptions. 


Ref:
1. https://www.esecurityplanet.com/threats/how-ransomware-uses-encryption-and-evolves/#:~:text=Ransomware%20can%20take%20your%20data,reverse%20operation%20without%20a%20key.

2. https://www.esecurityplanet.com/threats/lockfile-ransomware-evasion-rechniques/


Paper which is primarily referred:
Manabu Hirano, Ryo Hodota, Ryotaro Kobayashi,
RanSAP: An open dataset of ransomware storage access patterns for training machine learning models, Forensic Science International: Digital Investigation,
Volume 40,2022,301314,ISSN 2666-2817,
https://doi.org/10.1016/j.fsidi.2021.301314.

Visor I will be using is WaybackVisor:
Hirano, Manabu & Tsuzuki, Takuma & Ikeda, Seishiro & Taka, Naoga & Fujiwara, Kenji & Kobayashi, Ryotaro. (2017). WaybackVisor: Hypervisor-Based Scalable Live Forensic Architecture for Timeline Analysis. https://doi.org/10.1007/978-3-319-72395-2_21. 
