# Cloudflare load balancer (Pingora)

## Description

This is a fast runner for Cloudflare Pingora.
Cloudflare Pingora is Cloudflare Load Balancer used by Cloudflare for its service.

This can come handy to allow a bare-metal host within a DMZ to act as a load balancer instead of a service doing in the cloud. 

One can setup a setip.io account in transparent mode, connect the host in Transparent mode and run the load balancer directly on that host. The host obtains its public IP address from setip.io and Pingora can then listen to incoming connection just as if it was connected directly to the Internet with a fixed and static IP address.




## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Installation

Clone the project from terminal on your host, then read further to run it with default values or read the Configuration section to change default values such as the listening port and the list of origins to load balance to.

## Usage

Build the load balancer with:
`cargo build`

Run the load balancer with:
`cargo run`

## Configuration

Choose a port number for the load balancer and edit the main.rs file to reflect the port number if different:
Default port is 6188.
`lb.add_tcp("0.0.0.0:6188");`

Choose the local or remote IP addresses that the load balancer will balance between and replace the hard coded values:
` LoadBalancer::try_from_iter(["1.1.1.1:443", "1.0.0.1:443"]).unwrap();`

## Support

Contact information for getting support or reporting issues.

## Acknowledgements

## Credits and Acknowledgements

This project uses these external libraries:

- **Library Name**: [pingora](https://github.com/yourusername/pingora) (Replace with actual URL)
  - **Version**: 0.1
  - **License**: (Replace with actual license)
  - **Usage**: (Replace with actual usage)
  - **Features Used**: lb

- **Library Name**: [tokio](https://github.com/tokio-rs/tokio)
  - **Version**: 1
  - **License**: MIT
  - **Usage**: Tokio is a Rust framework for developing applications which perform asynchronous I/O — an event-driven approach that can often achieve better scalability, performance, and resource usage than conventional synchronous I/O.

- **Library Name**: [async-trait](https://github.com/dtolnay/async-trait)
  - **Version**: 0.1.42
  - **License**: Apache-2.0 OR MIT
  - **Usage**: This library allows you to use async/await syntax with your trait methods.

- **Library Name**: [httparse](https://github.com/seanmonstar/httparse)
  - **Version**: 1
  - **License**: MIT
  - **Usage**: httparse is a fast, minimal HTTP request/response parsing library.

- **Library Name**: [bytes](https://github.com/tokio-rs/bytes)
  - **Version**: 1.0
  - **License**: MIT
  - **Usage**: Bytes is a utility library for working with bytes.

- **Library Name**: [http](https://github.com/hyperium/http)
  - **Version**: 1.0.0
  - **License**: MIT/Apache-2.0
  - **Usage**: http is a library for types and traits for working with HTTP in Rust.

- **Library Name**: [log](https://github.com/rust-lang/log)
  - **Version**: 0.4
  - **License**: MIT/Apache-2.0
  - **Usage**: log provides a logging implementation for Rust.

- **Library Name**: [h2](https://github.com/hyperium/h2)
  - **Version**: >=0.4.2
  - **License**: MIT
  - **Usage**: h2 is a HTTP/2.0 client & server implementation for Rust.

- **Library Name**: [once_cell](https://github.com/matklad/once_cell)
  - **Version**: 1
  - **License**: MIT OR Apache-2.0
  - **Usage**: once_cell provides Rust library for single assignment cells and lazy statics without macros.

- **Library Name**: [lru](https://github.com/jeromefroe/lru-rs)
  - **Version**: 0
  - **License**: MIT
  - **Usage**: lru provides an implementation of least recently used caching algorithm in Rust.

- **Library Name**: [ahash](https://github.com/tkaitchuck/aHash)
  - **Version**: >=0.8.9
  - **License**: Apache-2.0 OR MIT
  - **Usage**: ahash is a high performance, (non-cryptographic) hashing algorithm.

