# IU Pressbooks Thin Common Cartridge Export Plugin

Thin CC Export for Pressbooks at IU. Based on the Candela LTI integration from Lumen Learning (https://github.com/lumenlearning/candela-thin-exports). 

Primary differences:

- Creates LTI links with Canvas extension for privacy setting set to "Public" allowing more identifying info to come across LTI. Facilitates SSO between LTI and Shibboleth on the WordPress side using the IU network ID as the WP username.

## Requirements

Requires the core WordPress LTI plugin from Lumen Learning (https://github.com/lumenlearning/lti) as well as the IU variant of Lumen's Pressbooks LTI plugin (also in this GitHub account).

## Publishing to IU's Unizin-hosted dev instance of Pressbooks.

### SSH shell connection

Public SSH key and IP address must be supplied to Unizin to whitelist an SSH connection to the server. Then SSH connections can be made from a shell terminal:

	ssh -i <path to your private key file> ubuntu@54.212.234.236

### SCP (file transfer)

Uploading files from your local machine to the server can be done using SCP (also requires the SSH key). Note that the local path is to the specific plugin's folder and the remote path is to the root of the plugins folder.

	scp -i <path your private key file> -r <local-path-of-the-specific-plugin-root> ubuntu@54.212.234.236:/var/www/iu-dev/wordpress/wp-content/plugins/
