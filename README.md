# AMI Winehouse
AMI Manager (to view / deregister Private AWS AMIs)

#Requirements

- [NodeJS](http://nodejs.org/)

#Installation/Setup

    git clone <this repo>
    npm install
    
#Options
- profile : (optional) Loads the profile from ~/.aws/credentials. If not specified, loads the 'default' profile. For details on how to configure the profiles, see [here](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-multiple-profiles)
- action : (optional) Acceptable values are 'list','deregister' . Default : 'list'
- region : (optional) Valid AWS Regions (more [here](http://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region))
- filterByState : (optional) Valid AMI State , currently supported : pending|available|failed
- pattern : (optional) A string pattern to match against the AMI name.
- help : (optional) Display a helpful usage message

#Example usage

    amy --pattern foo-bar- --filterByState available --action deregister
The above command will list all private AMIs with "foo-bar-" in their names in state 'available' and will request input for deregistration

# Bugs

Please report bugs [here](https://github.com/ivarrian/amiwinehouse/issues)
