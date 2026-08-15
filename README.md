# About
## Summary
DOI: 10.5281/zenodo.17624554

Gravity Falls is the repo named after an old cartoon comedy from the mid-2010s and a favored meme: "It's worthless!" and to differentiate from Pi-Hole's Gravity update process. DNS Sinkhole list of FQDNs from LevelBlue (AlienVault) OTX pivots by "MalwareMorghulis". Data was curated from automated and manual pivots to uncover suspicious or potentially hostile infrastructure. These monikers for campaign tracking are my own naming convention - unrelated to CrowdStrike, Mandiant, Palo Alto, etc. They are named for fun based on the TTP observed. Eventually, the lists will be reduced to regexes for maintenance purposes, ease of change-control, and due to UI limitations of LevelBlue OTX. Based on available open-source reporting, these DGA campaign activity clusters are likely associated with "Smishing Triad" (a cybercriminal group believed to be located in China).

**NOTE**: 2026_Research_Analysis\appendix.txt contains the command-line steps needed to replicate this experiment, due to documentation issues in originating tool source pages and tool results of the experiment.

## Research Block Lists
### DGA Tracker - Attributed to Smishing Triad
- **Cats Cradle**: SMS spearphishing utilizing random characters (approximately 5-9 characters)
- **Double Helix**: SMS spearphishing utilizing dual-word concatenation (even words are truncated)
- **Easy Rider**: Toll-themed or EZ-Pass themed SMS spearphishing utlizing random character concatenation or combo-lists.
- **Pandoras Box**: USPS-themed SMS Spearphishing Domains (typically package tracking or typo-squatting service offerings like Informed Delivery). This is not strictly package delivery. The cluster uses complex combo-lists with typosquats.

### Scam Tracker - Inconclusive
- **Empty Promise**: Fake recruiter spam, from emails, asking the user to contact them over third-party messengers: Telegram, WhatsApp, etc.
- **Purple Rain**: Indigo marketing and fake account notifications, including aliases Henry Fields or Daryl Huff.

### Replication & Results
- See here for the output tables or tested tool replication steps.

## Credits
### Citations
- For use, please cite Adam Dorian Wong (@MalwareMorghulis) & Dr. John Hastings.

### Special Thanks
1) Ian Campbell (DT) & **DomainTools** - for your support and helping me stay in the fight! The IRIS Investigate tool and DNSDB Scout are amazing tools! DomainTools has been an amazing supporter through their research program! Their tool has given us capabilities for long-term analysis in the DGA clusters and scalable access to data! Without them, this project wouldn't be possible - so huge thank you!
2) **ExtraHop** - for giving me the time & opportunity to pursue these side-hobby research objectives!
3) John Conwell (EH) - for supporting samples in helping track later phases of the campaign!
4) Dr. John Hastings (DSU) - for supporting the efforts to publish the research!
5) Dr. Cody Welu (DSU) - for supporting the research!

### Honorable Mentions - Thank you for your support!
1) Sublime Security
2) Epeios
3) Daniel P at Malpedia
4) Paul B at MalBeacon (Deception.Pro)
5) Hunt.io

### Disclaimer
- These lists are provided "as-is". This may break infrastructure because some nameservers could be in this list. Fork & prune or use at your own risk.
- **WARNING**: Please modify these TLD blocks as necessary and in your own repo. You have to point your PiHole to your own repo for any custom TLD blocklists because these TLD lists will block almost everything (even *.com, etc).
- **NOTE**: There are also way more efficient methods (ie: geolocation lists) or optimized entries to add TLDs into sinkholes, such as in single-line groupings with pipe '|' characters.

### References
- https://www.silentpush.com/blog/smishing-triad/
- https://krebsonsecurity.com/2025/04/china-based-sms-phishing-triad-pivots-to-banks/
- https://malpedia.caad.fkie.fraunhofer.de/actor/smishing_triad
- https://www.wired.com/story/smishing-triad-scam-group/
- https://www.resecurity.com/blog/article/smishing-triad-is-now-targeting-toll-payment-services-in-a-massive-fraud-campaign-expansion
