# iron-socket-io-client [![Build Status](https://travis-ci.org/Collaborne/iron-socket-io-client.svg?branch=master)](https://travis-ci.org/Collaborne/iron-socket-io-client) [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/Collaborne/iron-socket-io-client)  
[![Published on Vaadin  Directory](https://img.shields.io/badge/Vaadin%20Directory-published-00b4f0.svg)](https://vaadin.com/directory/component/Collaborneiron-socket-io-client)
[![Stars on vaadin.com/directory](https://img.shields.io/vaadin-directory/star/Collaborneiron-socket-io-client.svg)](https://vaadin.com/directory/component/Collaborneiron-socket-io-client)

Polymer element to connect to socket-IO

This element uses Polymer 2 native classes (ES6 syntax).

## Install

`bower install --save Collaborne/iron-socket-io-client`

## Usage

The component provides an imperative interface to connect to a Socket.IO server. The messages emitted by the server must use the event `message`, and must be objects with minimally a `type` property. Handlers can be defined based on (a prefix of) the `type` property of the messages.

1. Embed the component
2. Call `invoke(uri, [token])` to connect to the `/socket.io/` location at the given URI. The optional `token` argument will be used as 'Bearer' token in the `authorization` header of the initial request.
3. Call `registerHandler(typePrefix, handler)` to receive messages with their `type` property starting the with the prefix `typePrefix`. The handler is invoked with the complete message as argument, and any return value of the handler is ignored. All handlers matching a message are involved in the order of registration.
4. Call `send(message)` to send `message` events to the server, or `emit(type, message)` to emit events with the given type.

## License

    This software is licensed under the Apache 2 license, quoted below.

    Copyright 2011-2017 Collaborne B.V. <http://github.com/Collaborne/>

    Licensed under the Apache License, Version 2.0 (the "License"); you may not
    use this file except in compliance with the License. You may obtain a copy of
    the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
    License for the specific language governing permissions and limitations under
    the License.
