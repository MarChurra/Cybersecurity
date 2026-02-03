## Communication Protocols 
Rules, or protocols, are required in order for a message to be sucessfully delivered and understood.

### It´s required to:
  -An identified sender and receiver
  -Agreed upon method of communication
  -Common language and grammar
  -Speed and timing of delivery
  -Confirmation or acknolwedgement requirements

### Protcol Characteristics:
  -Message Format (A message needs to use a specific format or structure. Message formats depend on the type of message and the channel that is used to deliver it)
  -Message size (The rules that govern the size of the pieces communicatted across a network are very strict. They can also be different, depending on the channel used. When a long message is sent from one host to another, over a network, it may be necessary to break the message into smaller pieces, in order to ensure the message can be delivered.)
  -Timing (Many network communication functions are dependent on timing. it determines the speed at which the bits are transmitted across the network. It also affects when an individual host can send data and the total amount of data that can be sent in any one transmission)
  -Encoding (Messages sent across the network are first converted into bits by the sending host. Each bit is encoded into a pattern of sounds, light waves, or electrical impulses, depending on the network media over which the bits are transmitted. The destination host receives and decodes the signals in order to interpret the message)
  -Encapsulation (Each message transmitted on a network must include a ehader that contains adressing information that identifies the srouce and destination hosts. Encapsulation is the process of adding this information to the pieces of data that make up the message. In addition to adressing, there may be other information in the header that ensures that he message is devlivered to the correct application on the destination host.)
  -Message Pattern (Some messages require an acknowledgement before the enxt message can be sent. This type of request / response pattern is a common aspect of many networking protocols. However, there are other types of messages that may simply streamed across the network, without concern as to whether they reach their destination. )

With the increasing number of new devices, changes are managed via internet standards.
A standard is a set of rules that determines how something must be done. Networking and internet standards ensure that all devices connecting to the network implement the same set of rules or protocols, in the same manner. Using standards, it is possible for different types of devices to send information to each other over the internet. For example, the way in which an email is formatted, forwarded, and received by all devices is done according to a standard.

## Network Protocols:
  -Ethernet
  -IP
  -TCP
  -UDP
  -HTTP/HTTPS

## The TCP/IP Model

  ### TCP/IP Model Layers:
  -Application (Represents data to the user, plus enconding and dialog control )
  -Transport (Supports communication between various devices across diverse networks)
  - Internet (Determines the best path through the network )
  - Network Access (Controls the hardware devices and media that make up the network )

## OSI Reference Model 
