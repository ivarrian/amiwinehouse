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
- filterByStatus : (optional) Valid CloudFormation Stack Statuses (more [here](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html)). Specify more than one status separated by commas. If not specified, cf-manager will attempt to list stacks of all statuses. Please note that this may 
- pattern : (optional) A string pattern that the name(s) of CloudFormation stack(s) begin with. If not specified, cf-manager will attempt to list all cloudformation stacks. **Warning: Not specifying a status may exceed the throttle rate for API requests**
- help : (optional) Display a helpful usage message

#Example usage

    amy --pattern foo-bar- --filterByStatus available --action deregister
The above command will list all private AMIs with "foo-bar-" in their names and with status 'available' and will request input for deregistration

# Bugs

Please report bugs [here](https://github.com/ivarrian/amiwinehouse/issues)
