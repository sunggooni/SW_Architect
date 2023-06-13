<!-- Output copied to clipboard! -->

<!-----

Yay, no errors, warnings, or alerts!

Conversion time: 0.5 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β34
* Mon Jun 12 2023 19:25:30 GMT-0700 (PDT)
* Source doc: QA Scenarios
----->


#### QA scenario (Security): When a user tries to log in the server, the application shall connect to the server through a secure channel (e.g. TLS) to prevent the user's password from hackers.
- Stimulus: Sniff an user's password
- Source of stimulus: Hacker
- Artifact: Login Subsystem
- Environment/context: Try to log in
- Response: The hacker cannot sniff the user's password.
- Response measure: The user's password is encrypted through some encryption algorithm.

#### QA scenario (Usability): To add a contact to the list, the application shall provide search filters, such as last name, first name, address, e-mail or contact identifier.
- Stimulus: Search a user
- Source of stimulus: User
- Artifact: The list of user
- Environment/context: Add a contact to the list
- Response: The contact is added to the list successfully.
- Response measure: A user can be searched by last name, first name, address, e-mail, or contact identifier.

QA scenario (Performance): During a call, the application shall provide low latency communication. The latency shall be within 300ms and the jitter shall be within 300ms, so that the user cannot notice any disconnection.



* Stimulus: Transmit packets
* Source of stimulus: User
* Artifact: Communication module
* Environment/context: During a call
* Response: The user does not notice any latency or jitter.
* Response measure: Latency - within 300ms, Jitter - within 300ms

QA scenario (Availability): During monitoring bandwidth between two users, when the bandwidth is higher than 1.2Mbps (Up 600Kbps/Down 600Kbps) for 480p video call the application shall support the video call.



* Stimulus: Increase bandwidth
* Source of stimulus: Connection
* Artifact: Application
* Environment/context: Monitor bandwidth during a call
* Response: Video call is supported.
* Response measure: The bandwidth between two users is higher than 1.2Mbps (Up 600Kbps / Down 600Kbps)

QA scenario (Availability): During a call, the application shall adjust the bandwidth according to the codec that the user uses. The minimum bandwidths for each codec are described later.



*  Stimulus: Change codec
*  Source of stimulus: User
*  Artifact: Communication module
*  Environment/context: During a call
*  Response: The bandwidth is adjusted according to the codec.
*  Response measure: There are the minimum bandwidths for each codec.

QA scenario (Security): When the application tries to connect to the server or the other user, the connection between them shall be secured through a secure channel (e.g. TLS) to prevent the user’s information and calls from hackers.



* Stimulus: Sniff users’ informatoin and call
* Source of stimulus: Hacker
* Artifact: Communication
* Environment/context: Normal operation
* Response: The hacker cannot sniff the users’ information and calls.
* Response measure: The users’ information and calls are encrypted through some encryption algorithm.

QA scenario (Availability): When the application fails to connect to the other user, it shall retry to connect every 3 seconds. Before retrying, the application confirm if the IP address of peer changes through the server. After retrying 5 times, the application shall inform the user of the dropped call.



*  Stimulus: Detect dropped call
*  Source of stimulus: Application
*  Artifact: Communication module
*  Environment/context: Try to call
*  Response: Call is connected
*  Response measure: Retry to connect 5 times after timeout of 3 seconds

QA scenario (Availability): When the IP address of the application changes, the application shall inform the server of the new IP address as soon as possible. The server shall update the changed IP address in the storage. This change is notified the server within 10 seconds before other users fail to call.



*  Stimulus: Change IP address of the application
*  Source of stimulus: Application
*  Artifact: Server
*  Environment/context: Normal operation
*  Response: The IP address stored in the server changes.
*  Response measure: The change is notified the server within 10 seconds.

QA scenario (Modifiability): Source codes for usage of codecs and/or encryption algorithms shall be encapsuled so that the developer or maintainer can easily add or replace them. In the top of the codes and/or encryption algorithms, there shall be an adaptation layer for them.



*  Stimulus: Add or replace codecs and/or encryption algorithms
*  Source of stimulus: Developer/maintainer
*  Artifact: Source code
*  Environment/context: Development phase
*  Response: Codecs and/or encryption algorithms are added easily.
*  Response measure: 10 person-days effort.

QA scenario (Security): The server shall store the users’ passwords in chipertext to prevent hackers from getting them. The chipertext can be created by hash algorithms.



*  Stimulus: Try to see the users’ passwords
*  Source of stimulus: Hacker
*  Artifact: Server storage
*  Environment/context: Normal operation
*  Response: Hackers cannot see the users’ passwords in plaintext.
*  Response measure: The user’s passwords are stored in chipertext.

QA scenario (): 



*  Stimulus: 
*  Source of stimulus: 
*  Artifact: 
*  Environment/context: 
*  Response: 
*  Response measure: 

QA scenario (): 



*  Stimulus: 
*  Source of stimulus: 
*  Artifact: 
*  Environment/context: 
*  Response: 
*  Response measure: 
