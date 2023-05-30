# Network Intrusion Detection System Using ML

The proposed work is implemented in Python 3.11 with libraries scikit-learn, pandas, matplotlib and other mandatory libraries. We downloaded dataset from kdd.ics.uci.edu. The data downloaded contains train set and test set separately with four different classes of intrusions. The train dataset considered as train set and test dataset considered as test set. 
We have collected the dataset for the intrusion detection system with following details from KDD dataset. For our dataset we have selected various classification techniques such as:
 
1.	Logistic Regression
2.	Decision Tree
3.	K-Nearest Neighbors
4.	Naive bayes Model
5.	Support Vector Machine (SVM)
6.	Neural Network Model
 
### DATA AVAILABILITY: 

This data is KDDCUP’99 data set, which is widely used as one of the few publicly available data sets for network-based anomaly detection systems.  
 
For more about data: http://www.unb.ca/cic/datasets/nsl.html 

#### LIST OF COLUMNS FOR THE DATA SET:

["duration","protocol_type","service","flag","src_bytes","dst_bytes","land", "wrong_fragment","urgent","hot","num_failed_logins","logged_in", "num_compromised","root_shell","su_attempted","num_root","num_file_creations", "num_shells","num_access_files","num_outbound_cmds","is_host_login", "is_guest_login","count","srv_count","serror_rate", "srv_serror_rate", "rerror_rate","srv_rerror_rate","same_srv_rate", "diff_srv_rate", 
"srv_diff_host_rate","dst_host_count","dst_host_srv_count","dst_host_same_srv_rate", "dst_host_diff_srv_rate","dst_host_same_src_port_rate", "dst_host_srv_diff_host_rate","dst_host_serror_rate","dst_host_srv_serror_rate", "dst_host_rerror_rate","dst_host_srv_rerror_rate","attack", "last_flag"]

#### BASIC FEATURES OF EACH NETWORK CONNECTION VECTOR:

1) <b>Duration:</b>  Length of time duration of the connection  
2) <b>Protocol_type:</b> Protocol used in the connection  
3) <b>Service:</b> Destination network service used  
4) <b>Flag:</b> Status of the connection – Normal or Error 
5) <b>Src_bytes:</b> Number of data bytes transferred from source to destination in single connection  
6) <b>Dst_bytes:</b> Number of data bytes transferred from destination to source in single connection  
7) <b>Land:</b> if source and destination IP addresses and port numbers are equal then, this variable takes value 1 else 0  
8) <b>Wrong_fragment:</b> Total number of wrong fragments in this connection  
9) <b>Urgent:</b> Number of urgent packets in this connection. Urgent packets are packets with the urgent bit activated

#### CONTENT RELATED FEATURES OF EACH NETWORK CONNECTION VECTOR:

10) <b>Hot:</b> Number of "hot" indicators in the content such as: entering a system directory, creating programs and executing programs 
11) <b>Num_failed _logins:</b> Count of failed login attempts  
12) <b>Logged_in Login Status:</b> 1 if successfully logged in; 0 otherwise  
13) <b>Num_compromised:</b> Number of "compromised" conditions  
14) <b>Root_shell:</b> 1 if root shell is obtained; 0 otherwise  
15) <b>Su_attempted:</b> 1 if "su root" command attempted or used; 0 otherwise  
16) <b>Num_root:</b> Number of "root" accesses or number of operations performed as a root in the connection 
17) <b>Num_file_creations:</b> Number of file creation operations in the connection  
18) <b>Num_shells:</b> Number of shell prompts  
19) <b>Num_access_files:</b> Number of operations on access control files  
20) <b>Num_outbound_cmds:</b> Number of outbound commands in an ftp session  
21) <b>Is_hot_login:</b> 1 if the login belongs to the "hot" list i.e., root or admin; else 0  
22) <b>Is_guest_login:</b> 1 if the login is a "guest" login; 0 otherwise 

#### TIME RELATED TRAFFIC FEATURES OF EACH NETWORK CONNECTION VECTOR:

23) <b>Count:</b> Number of connections to the same destination host as the current connection in the past two seconds 
24) <b>Srv_count:</b> Number of connections to the same service (port number) as the current connection in the past two seconds  
25) <b>Serror_rate:</b> The percentage of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in count (23)  
26) <b>Srv_serror_rate:</b> The percentage of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in srv_count (24)  
27) <b>Rerror_rate:</b> The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in count (23)  
28) <b>Srv_rerror_rate:</b> The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in srv_count (24)  
29) <b>Same_srv_rate:</b> The percentage of connections that were to the same service, among the connections aggregated in count (23)  
30) <b>Diff_srv_rate:</b> The percentage of connections that were to different services, among the connections aggregated in count (23)
31) <b>_diff_host_ rate:</b> percentage of connections that were to different destination machines among the connections aggregated in srv_count (24) 

####  HOST BASED TRAFFIC FEATURES IN A NETWORK CONNECTION VECTOR:

32) <b>Dst_host_count:</b> Number of connections having the same destination host IP address  
33) <b>Dst_host_srv_ count:</b> Number of connections having the same port number  
34) <b>Dst_host_same _srv_rate:</b> The percentage of connections that were to the same service, among the connections aggregated in dst_host_count (32)  
35) <b>Dst_host_diff_ srv_rate:</b> The percentage of connections that were to different services, among the connections aggregated in dst_host_count (32)  
36) <b>Dst_host_same _src_port_rate:</b> The percentage of connections that were to the same source port, among the connections aggregated in dst_host_srv_c ount (33)  
37) <b>Dst_host_srv_ diff_host_rate:</b> The percentage of connections that were to different destination machines, among the connections aggregated in dst_host_srv_count (33) 
38) <b>Dst_host_serro r_rate:</b> The percentage of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in dst_host_count (32)  
39) <b>Dst_host_srv_s error_rate:</b> The percent of connections that have activated the flag (4) s0, s1, s2 or s3, among the connections aggregated in dst_host_srv_c ount (33)  
40) <b>Dst_host_rerro r_rate:</b> The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in dst_host_count (32)  
41) <b>Dst_host_srv_r error_rate:</b> The percentage of connections that have activated the flag (4) REJ, among the connections aggregated in dst_host_srv_c ount (33) 


### Attack Class : Attack Type
              
1) DoS       : Back, Land, Neptune, Pod, Smurf,Teardrop,Apache2, Udpstorm, Processtable, Worm (10) 

2) Probe     : Satan, Ipsweep, Nmap, Portsweep, Mscan, Saint  (6) 

3) R2L       : Guess_Password, Ftp_write, Imap, Phf, Multihop, Warezmaster, Warezclient, Spy, Xlock, Xsnoop, Snmpguess, Snmpgetattack, Httptunnel, Sendmail, Named (16)
 
4) U2R       : Buffer_overflow, Loadmodule, Rootkit, Perl, Sqlattack, Xterm, Ps (7) 

### ATTACK CLASS: 

1. <b>DOS:</b> Denial of service is an attack category, which depletes the victim‟s resources thereby making it unable to handle legitimate requests – e.g. syn flooding. Relevant features: “source bytes” and “percentage of packets with errors”  
2. <b>Probing:</b> Surveillance and other probing attack‟s objective is to gain information about the remote victim e.g. port scanning. Relevant features: “duration of connection” and “source bytes”  
3. <b>U2R:</b> unauthorized access to local super user (root) privileges is an attack type, by which an attacker uses a normal account to login into a victim system and tries to gain root/administrator privileges by exploiting some vulnerability in the victim e.g. buffer overflow attacks. Relevant features: “number of file creations” and “number of shell prompts invoked,” 
4. <b>R2L:</b> unauthorized access from a remote machine, the attacker intrudes into a remote machine and gains local access of the victim machine. E.g. password guessing Relevant features: Network level features – “duration of connection” and “service requested” and host level features - “number of failed login attempts” 


Project Inspired By:
https://github.com/vicky60629/Network-Intrusion-Detection-System
