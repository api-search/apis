---
aid: command-line-interface:posix-utility-conventions
baseURL: https://pubs.opengroup.org
description: The POSIX Utility Conventions specify the expected behavior of command line utilities including argument parsing, flag styles, end-of-options separators, and exit status. Following POSIX makes a tool feel native to UNIX-like environments and predictable when composed in pipelines and shell scripts.
humanURL: https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html
image: ''
layout: api
name: POSIX Utility Conventions
properties:
- type: Specification
  url: https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html
- type: Reference
  url: https://www.gnu.org/software/libc/manual/html_node/Argument-Syntax.html
provider_name: Command Line Interface
provider_slug: command-line-interface
slug: posix-utility-conventions
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: command-line-interface:posix-utility-conventions\nname: POSIX Utility Conventions\ndescription: The POSIX Utility Conventions specify the expected behavior of command line utilities including\n  argument parsing, flag styles, end-of-options separators, and exit status. Following POSIX makes a tool\n  feel native to UNIX-like environments and predictable when composed in pipelines and shell scripts.\nhumanURL: https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html\nbaseURL: https://pubs.opengroup.org\ntags:\n- Conventions\n- POSIX\n- Standards\n- UNIX\nproperties:\n- type: Specification\n  url: https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html\n- type: Reference\n  url: https://www.gnu.org/software/libc/manual/html_node/Argument-Syntax.html\nx-features:\n- Defines short flags, long flags, and option arguments\n- Specifies the `--` end-of-options sentinel\n- Standardizes exit status conventions\n- Foundation for getopt and getopts\
  \ utilities\nx-useCases:\n- Writing portable CLI utilities for UNIX-like systems\n- Implementing argument parsers that match user expectations\n- Documenting tool behavior in man pages\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/command-line-interface/refs/heads/main/apis.yml
tags:
- Conventions
- POSIX
- Standards
- UNIX
---
