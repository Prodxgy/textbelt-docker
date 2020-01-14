# Textbelt-Docker
A docker image and compose to easily run [textbelt](https://github.com/typpo/textbelt), and send outgoing SMS messages through Carrier Email-to-SMS Gateways.

## INSTALLATION
*git, docker, and docker-compose must be installed*

1. `git clone https://github.com/hexeth/textbelt-docker.git`
1. `cd textbelt-docker`
1. `nano docker-compose.yml`, set your env variables (listed below), save and exit
1. run `docker-compose up -d` 

## ENV VARIABLES
* `HOST` **= smtp.host.com** *#your smtp domain address: default is smtp.gmail.com*
* `MAIL_PORT` **= 587** *#your smtp port: default is 587*
* `MAIL_USER` **= youremailaccount** *#your email account name including domain*
* `MAIL_PASS` **= youremailpassword** *#your email account password*
* `FROM` **= youremailaddress** *#your from email address: myemail@domain.com*
* `REALNAME` **= your name** *#your name that appears in from email*
* `MAIL_DEBUG` **= true** *#debug mailing: default false*
* `SECURE_CONNECTION` **= false** *#if ssl is required: default is false*

## USAGE

* Run the following command `curl -X POST http://127.0.0.1:9090/text --data-urlencode number='18001337' --data-urlencode carrier='att' --data-urlencode 'message=Hello world'`
* Replace /text with /canada for canadian carriers or /intl for international carriers (supported carriers below).


## SUPPORTED CARRIERS
* Supported U.S. carriers: Alltel, Ameritech, AT&T Wireless, Boost, CellularOne, Cingular, Edge Wireless, Nex-Tech Wireless, Project Fi, Sprint PCS, Telus Mobility, T-Mobile, Metro PCS, Nextel, O2, Orange, Qwest, Rogers Wireless, Ting, US Cellular, Verizon, Virgin Mobile.

* Supported U.S. and Canadian carriers (/canada): 3 River Wireless, ACS Wireless, AT&T, Alltel, BPL Mobile, Bell Canada, Bell Mobility, Bell Mobility (Canada), Blue Sky Frog, Bluegrass Cellular, Boost Mobile, Carolina West Wireless, Cellular One, Cellular South, Centennial Wireless, CenturyTel, Cingular (Now AT&T), Clearnet, Comcast, Corr Wireless Communications, Dobson, Edge Wireless, Fido, Golden Telecom, Helio, Houston Cellular, Idea Cellular, Illinois Valley Cellular, Inland Cellular Telephone, MCI, MTS, Metro PCS, Metrocall, Metrocall 2-way, Microcell, Midwest Wireless, Mobilcomm, Nextel, OnlineBeep, PCS One, President's Choice, Public Service Cellular, Qwest, Republic Wireless, Rogers AT&T Wireless, Rogers Canada, Satellink, Solo Mobile, Southwestern Bell, Sprint, Sumcom, Surewest Communicaitons, T-Mobile, Telus, Tracfone, Triton, US Cellular, US West, Unicel, Verizon, Virgin Mobile, Virgin Mobile Canada, West Central Wireless, Western Wireless

* Supported international carriers (/intl): Chennai RPG Cellular, Chennai Skycell / Airtel, Comviq, DT T-Mobile, Delhi Aritel, Delhi Hutch, Dutchtone / Orange-NL, EMT, Escotel, German T-Mobile, Goa BPLMobil, Golden Telecom, Gujarat Celforce, JSM Tele-Page, Kerala Escotel, Kolkata Airtel, Kyivstar, LMT, Lauttamus Communication, Maharashtra BPL Mobile, Maharashtra Idea Cellular, Manitoba Telecom Systems, Meteor, MiWorld, Mobileone, Mobilfone, Mobility Bermuda, Mobistar Belgium, Mobitel Tanzania, Mobtel Srbija, Movistar, Mumbai BPL Mobile, Netcom, Ntelos, O2, O2 (M-mail), One Connect Austria, OnlineBeep, Optus Mobile, Orange, Orange Mumbai, Orange NL / Dutchtone, Oskar, P&T Luxembourg, Personal Communication, Pondicherry BPL Mobile, Primtel, SCS-900, SFR France, Safaricom, Satelindo GSM, Simple Freedom, Smart Telecom, Southern LINC, Sunrise Mobile, Surewest Communications, Swisscom, Telcel Mexico, T-Mobile Austria, T-Mobile Germany, T-Mobile UK, TIM, TSR Wireless, Tamil Nadu BPL Mobile, Tele2 Latvia, Telefonica Movistar, Telenor, Teletouch, Telia Denmark, UMC, Uraltel, Uttar Pradesh Escotel, Vessotel, Vodafone Italy, Vodafone Japan, Vodafone UK, Wyndtell
