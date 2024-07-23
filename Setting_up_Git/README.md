# _*Setting Up Git*_

## _*Installing Git*_

- To use Git, you'll need to install it on your local machine. Follow these steps:

## _*Install Git for your Operating System*_

- Windows: Download and install Git from the official Git website: [Link](https://git-scm.com/downloads)

- macOS: Open the Terminal app and run the following command: ``brew install git``

- Linux: Open a terminal and run the following command: ``sudo apt-get install git`` (for Ubuntu-based systems) or ``sudo yum install git`` (for RHEL-based systems)

## _*Configuring Git*_

- After installing Git, you'll need to configure it with your username and email address. Run the following commands in your terminal:

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

- Replace "Your Name" and "<your_email@example.com>" with your actual name and email address.

### _*Verifying the Configuration*_

- To verify that your configuration is correct, run:

```bash
git config --global --list
```

- This should output a list of your configuration settings, including your username and email address.

- That's it! You're now set up to use Git on your local machine.
