# Rcode-for-Microbiome

## In this repo I save some scripts, exercise, and tutorial for analyzing microbiome data. However, first thign first, we need to instal `R` and `Rstudio`, so let's get started!

* #### Installing *R*

First thing is to remove the old version of R, remove any remaining packages, existing entry for R, then install some required libraries and finally reinstall R. In Ubuntu 18.04.6 LTS (Bionic Beaver) I did:

```
sudo apt remove r-base* --purge
sudo rm /home/gian/R/ -rf
sudo rm /home/gian/.r/
sudo rm /usr/lib/R/ -rf
```

Then open the sources.list file and remove or `#` any existing entry for R, e.g. :
```
sudo nano /etc/apt/sources.list
# deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/`
```
Install these required lirbaries:

```
sudo apt install libssl-dev libcurl4-openssl-dev libxml2-dev
```

And then add GPG key, R Repositiry, and install R again:

```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
sudo add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran40/'
sudo apt update
sudo apt install r-base
sudo -i R
```

* #### Installing *R Studio*

Download the deb file from the [Rstudio website](https://www.rstudio.com/) and then install it:

```
sudo apt install -f ./Downloads/rstudio-2021.09.2-382-amd64.deb
```
