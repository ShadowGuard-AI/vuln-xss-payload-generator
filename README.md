# vuln-XSS-Payload-Generator
Encodes and filter-simulates a single XSS payload that the operator supplies, and can list four built in example payloads. It does not generate new payloads and it has no target: nothing is sent anywhere and nothing it prints is executed. The filter option simulates a naive single pass filter that removes one chosen string once per occurrence pattern, so a filtered result can still be active markup; treat it as a simulation of that filter style, not as sanitization.

## Install
`git clone https://github.com/ShadowGuardAI/vuln-xss-payload-generator`

## Usage
`./vuln-xss-payload-generator [params]`

## Parameters
- `-h`: Show help message and exit
- `-p`: Base payload to encode or filter. Required unless `-l` is used.
- `-e`: Encoding type: html, url, none. Default: none
- `-f`: Filter string to remove from the payload, simulating a single pass filter
- `-l`: List the four built in example payloads.
- `-o`: Output file to write the resulting payload to.

Exit codes are honest: omitting `-p` without `-l`, or an encoding or filter error, exits non-zero.

## License
Copyright (c) ShadowStrikeHQ
