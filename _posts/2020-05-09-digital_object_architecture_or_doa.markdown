---
layout: post
title:      "Digital Object Architecture or DOA"
date:       2020-05-09 19:54:59 +0000
permalink:  digital_object_architecture_or_doa
---


DOA, otherwise known as Digital Object Architecture or DO Architecture. Which is a logical extension of the internet architecture. It addresses the need to support information management more generally. Rather than, just conveying the in information in a digital form from one location in the Internet to another. It enables interoperability across participating information systems. Whether it be in the Internet or not!! How cool is that!!! 

 It is a non-proprietary architecture and is publicly available!!!!!


Digital Object Architecture intorduces the concept of a digital object, which forms the basis for the architecture. Kind of like the foundation to a building. It specifies three (3) core componenets and two (2) protocols. Which are???

Well first lets get into what a digital object is. A digital object, or DO, is a sequence of bits or a set of sequences of bits that are incorporating a work or a portion of work or other information in which a person or party has rights or interests, in which there is a value. Each of the sequences being setup or structured in a way that is interpretable by one or more computational facilities, and having as an essential element, an associated unique persisten identifier.
For any and all pratical purposes, the concept of a DO is very close to the notion of a 'digital entity' (as defined in ITU-T Recommendation X.1255 that was based largely on the Digital Object Architecture.) An 'entity' is defined as anything that can be separately and uniquely identified. It also describes a DE or 'digital entity' that is represented as, or convered to a machine-independent data structure. Which also constits of one or more elements that may be parsed by different systems. 

Now, to the two protocols!!!

DIOP - Digital Object Interface Protocol is a simple, but powerful conceptual protocol for software applications to interact with “services” which could be either the DOs or the information systems that manage those DOs.

IRP - Identifier/Resolution Protocol is a rapid-resolution protocol for creating, updating, deleting, and resolving identifiers that are globally managed and allotted. Each identifier is associated with a record that clients can resolve to using this protocol.

And now to the three core components that I mentioned earlier!!! 

The Identifier/Resolution System

This is one of the three components comprising the Digital Object Architecture. This enables: 
1. Allotment of unique identifiers to information in digital form structured as digital objects regardless of the location of     such information or the technology used to serve such information, and subsequently, and
2. The resolution of the identifiers to current state information about the corresponding digital object, e.g., its 
     location(s), access & usage policies, timestamps, and/or public keys.
		 
The state information is stored in the form of a digital object; and rapid resolution is enabled using the IRP.

The Respository System

This system manages DOs including the provision of access to such objects based on the use of identifiers and with integrated security. Through the use of identifiers in the access protocol, the repository system abstracts away the details of the storage technologies from the clients enabling a long-lived mechanism for depositing and accessing DOs.

Access to this system is enabled using the DOIP.

The Registry System

This particular system is a specialized repository system intended to store metadata about DOs rather than the digital information itself, and typically stores metadata of digital objects that are managed by one or more repository systems.

Access to this system is enabled using the DOIP also.

After I read this, I was confused as all get out. That is until I went through and did some digging in the course work. After I re-read the course work, it made more sense. I had to refresh my memory on some terminology. Once I did that it made more sense to me. And after realizing what it was talking about and how it all worked, I was blown away. Granted it can be put into more detail but I would rather leave that to the reader. If you are more interested in it then do the work and get your brain working. It is amazing and worth it!!!!
