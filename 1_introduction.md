# Introduction

Equation Consulting, Inc ("Equation") is committed to ensuring the confidentiality, privacy, integrity, and availability of all electronic protected health information (ePHI) it receives, maintains, processes and/or transmits on behalf of its clients. As providers of compliant, hosted infrastructure used by healthcare enterprises, Equation strives to maintain compliance, proactively address information security, mitigate risk for its clients, and assure known breaches are completely and effectively communicated in a timely manner. The following documents address core policies used by Equation to maintain compliance and assure the proper protections of infrastructure used to store, process, and transmit ePHI for Equation clients.

Equation provides secure and compliant cloud-based software. This hosted software is referred to as DataRiver and is a Platform as a Service (Paas).


## DataRiver (PaaS)

DataRiver is a cloud based solution that hosts customer data. The customers data is deployed into compliant containers that run on systems secured and managed by Equation. Equation makes every effort to reduce the risk of unauthorized disclosure, access, and/or breach of PaaS client data through network (firewalls, dedicated IP spaces, etc) and server settings (encryption at rest and in transit, log event management throughout the Platform, etc).


## Compliance Inheritance

Equation provides secure and compliant cloud-based software for its clients. Equation has been through a HIPAA compliance audit by a national, 3rd party compliance firm, to validate and map organizational policies and technical settings to HIPAA rules. Equation is currently undergoing a HITRUST audit to achieve HITRUST Certification.

Equation signs business associate agreements (BAAs) with its clients. These BAAs outline Equation obligations and client obligations, as well as liability in the case of a breach. In providing infrastructure and managing security configurations that are a part of the technology requirements that exist in HIPAA and HITRUST, as well as future compliance frameworks. The aspects of compliance related to Equation hosting client data are inherited by client entities, and Equation assumes the risk associated with those aspects of compliance. In doing so, Equation helps clients achieve and maintain compliance, as well as mitigates client risk.

Certain aspects of compliance cannot be inherited. Because of this, Equation Customers, in order to achieve full compliance or HITRUST Certification, must implement certain organizational policies. These policies and aspects of compliance fall outside of the services and obligations of Equation.

Below are mappings of HIPAA Rules to Equation controls and a mapping of what Rules are inherited by clients.


## Equation Organizational Concepts

The physical infrastructure environment is hosted at a secure Equation facility. These servers are physically secured in a temperature and moisture controlled environment, with 24x7 audio/video monitoring.  This monitoring includes temperature, humidity and movement (notification of any movement captured by video surveillance) alerts. The Equation environment consists of Cisco firewalls, Apache web servers, database servers, logging servers, monitoring servers, access control servers and OSSIM server.

Within the DataRiver Platform, all data transmission is encrypted and all hard drives are encrypted so data at rest is also encrypted; this applies to all servers and backups. Equation assumes all data *may* contain ePHI, even though our Risk Assessment does not indicate this is the case, and provides appropriate protections based on that assumption.

Equation has a multi-tenant data architecture and isolates tenant data in separate databases and instances. Computing resources and application code are generally shared between all the tenants on a server, but each tenant has its own set of data that remains logically isolated from data that belongs to all other tenants. Metadata associates each database with the correct tenant, and database security prevents any tenant from accidentally or maliciously accessing other tenants' data.


Additionally, IPtables is used on each each server for logical segmentation. The IPtables are configured to restrict access to only justified ports and protocols. Equation has implemented strict logical access controls so that only authorized personnel are given access to the internal management servers. The environment is configured so that data is transmitted to the application servers over an SSL encrypted session.


The Apache web server, DataRiver application servers are externally facing and accessible via the Internet. The database servers, where the ePHI resides, are located on the internal Equation network and can only be accessed directly over an SSH connection. The access to the internal database is restricted to a limited number of personnel and strictly controlled to only those personnel with a business justified reason. All points and occurrences of data access are logged and reviewed.  The system will automatically remove access for users if no activity is detected for a specified period.

All operating systems are tested end-to-end for usability, security and impact prior to deployment to production.

## Version Control

Policies were last updated April 11th, 2014.
