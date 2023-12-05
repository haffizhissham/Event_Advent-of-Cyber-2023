# Day 4: [Brute-forcing] Baby, it's CeWLd outside
Additional walktrough [video](https://www.youtube.com/watch?v=O2PJ_RzWp9g)


## Required Tools
1. **CeWL** (pronounced "cool")
   * Install CeWL if it's not available in your VM
     * ```sudo apt-get install cewl -y```
   * Features:
     * CeWL crafts wordlists specifically from the content of a targeted website.
     * CeWL can spider a website to a specified depth
     * Provides various options to fine-tune the wordlist
     * Includes functionalities such as username enumeration from author meta tags and email extraction
     * Integration with other tools, can be integrated seamlessly into automated workflows
     * Actively maintained and updated
   * Customise the Output for Specific Tasks
     * Specify spidering depth:
       * The ```-d``` option allows you to set how deep CeWL should spider. For example, to spider two links deep: ```cewl http://MACHINE_IP -d 2 -w output1.txt```
     * Set minimum and maximum word length: 
       *  Use the ```-m``` and ```-x``` options respectively. For instance, to get words between 5 and 10 characters: cewl ```http://MACHINE_IP -m 5 -x 10 -w output2.txt```
     * Handle authentication:
       *  If the target site is behind a login, you can use the ```-a``` flag for form-based authentication.
     * Custom extensions:
       *  The ```--with-numbers``` option will append numbers to words, and using ```--extension``` allows you to append custom extensions to each word, making it useful for directory or file brute-forcing.
     * Follow external links:
       *  By default, CeWL doesn't spider external sites, but using the ```--offsite``` option allows you to do so.
2. **wfuzz**, Brute-force tool

## Steps
1. Use CeWL (pronounced "cool") to generate wordlist by spidering the website
   * CeWL crafts wordlists specifically from the content of a targeted website (spidering).
   * CeWL can spider a website to a specified depth
   * Provides various options to fine-tune the wordlist
   * Includes functionalities such as username enumeration from author meta tags and email extraction
   * Integration with other tools, can be integrated seamlessly into automated workflows
   * Actively maintained and updated


2. Connect to the TryHackMe's VPn (or use AttackBox)



3. Customise the Output for Specific Tasks
   * Specify spidering depth:
     * The ```-d``` option allows you to set how deep CeWL should spider. For example, to spider two links deep: ```cewl http://MACHINE_IP -d 2 -w output1.txt```
   * Set minimum and maximum word length: 
     *  Use the ```-m``` and ```-x``` options respectively. For instance, to get words between 5 and 10 characters: cewl ```http://MACHINE_IP -m 5 -x 10 -w output2.txt```
   * Handle authentication:
     *  If the target site is behind a login, you can use the ```-a``` flag for form-based authentication.
   * Custom extensions:
     *  The ```--with-numbers``` option will append numbers to words, and using ```--extension``` allows you to append custom extensions to each word, making it useful for directory or file brute-forcing.
   * Follow external links:
     *  By default, CeWL doesn't spider external sites, but using the ```--offsite``` option allows you to do so.
