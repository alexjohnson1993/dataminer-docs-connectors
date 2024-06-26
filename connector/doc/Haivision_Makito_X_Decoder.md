---
uid: Connector_help_Haivision_Makito_X_Decoder
---

# Haivision Makito X Decoder

The Makito X decoder delivers dual-channel HD digital video to 3G-SDI and HDMI interfaces, supporting all HD standards up to 1080p60. The Makito X decoder is a unique match for the Makito X encoder.

The **Haivision Makito X Decoder** connector is used to monitor and control the decoder device. It provides an overview of the different parameters of the device, along with its statuses and generated alarms. The connector uses SNMP to retrieve the data from the device.

## About

### Version Info

| Range              | Key Features               | Based on | System Impact |
|--------------------|----------------------------|----------|---------------|
| 1.0.0.x            | Initial version            | -        | -             |
| 1.0.1.x [SLC Main] | New HTTP connection added. | -        | -             |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | 2.2.0-43               |
| 1.0.1.x   | 1.3.2-10               |

### System Info

| Range   | DCF Integration                                                        | Cassandra Compliant |
|---------|------------------------------------------------------------------------|---------------------|
| 1.0.0.x | No                                                                     | Yes                 |
| 1.0.1.x | No (prior to version 1.0.1.9) <br> Yes (starting from version 1.0.1.9) | Yes                 |

## Configuration

### Connections

#### SNMP Main Connection (range 1.0.0.x)

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

SNMP Settings:

- **IP port**: The IP port of the device.
- **Get community string**: The community string used when reading values from the device, by default *skyline*.
- **Set community string**: The community string used when setting values on the device, by default *private*.

#### HTTP Connection (range 1.0.1.x)

From range 1.0.1.x onwards, this connector uses an HTTP connection and requires the following input during element configuration:

HTTP CONNECTION:

HTTP Settings:

- **IP port**: The IP port of the device. Default value: *443*.
- **Bus Address**: The bus address used on the connection. Default value: *bypassproxy*.

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## Usage

### General

This page displays status information about the Makito X Decoder, such as the **Serial Number**, **Firmware Version**, **Firmware Date**, and **System Status**.

### Streams

This page contains detailed information concerning streams, including **Statistics**, **Content**, and **Programs**.

### Video

This page displays tables containing video information about **Inputs, Outputs**, and **Decoders**.

### Audio

This page displays **Audio Decoders** information, such as the related **statistics**. It also provides access to a subpage regarding the **Talkback Channels.**

### Services

This page displays the current status of **network services**.

### Logo

On this page, there is an entry for each **logo file** present in the system, as well as a **logo overlay** entry for each video input.

### Snapshot

This page contains a table with an entry for each **image snapshot** file in the system.

### Network

On this page, you can modify the network interface settings for the decoder, including **Ethernet** and **IP Address**.

It also contains page buttons to subpages with **DNS** (Domain Name Space) and **NTP** (Network Time Protocol) information.

### Web Interface

On this page you can access the web interface of the device. Note that the client machine has to be able to access the device, as otherwise it will not be possible to open the web interface.

### DCF Connections

#### External Connections

In version 1.0.1.9, DCF interfaces are generated for each stream in order to facilitate DCF connections.

DCF can also be implemented through the DataMiner DCF user interface and through third-party DataMiner connectors (e.g. a manager).
