# ![Concordant Logo](./concordant-logo-dark.svg#gh-dark-mode-only) ![Concordant Logo](./concordant-logo-light.svg#gh-light-mode-only)

Welcome to the Concordant source code repository. Concordant is an open-source local-first datastore with rich-CRDTs.

## About Concordant

The Concordant platform enables developers to create edge and mobile apps easily and quickly, with a uniform architecture extending across the edge and to the cloud.

The Concordant Client (C-Client) lightweight and portable design make it easy to run on all JS browsers, mobile phones and Unix hardware.

It was created to help web and mobile developers build applications that work as well offline as they do online. It enbales applications to store data locally while offline, then synchronise it with comptaible servers when the application is back online, keeping the user's data in sync no matter where they next login. Plus, the data is synchronised between clients, so usrs stay up-to-date whenever they go.

Apps built on top of Concordant offer:

- **Edge First:** data is available immediately and consistently, whenever needed;
- **Consistent by design:** share updates from diffenrent users, with clear, intuitive results;
- **Simple API:** Require some programming knowledge, however Concordant is a piece of cake to learn;
- **Uniforme semantics:** run app on edge device, in gateway, serverless, on in Cloud;
- **Secure:** end-to-end encryption and access control;
- **Open Source:** Everything is developed out in the open on GitHub, contributors always welcome!

More information:

- [Concordant Website](https://concordant.io)
- [Vision Paper](https://concordant.io/uploads/visionpaper-concordant_2020.pdf)
- [Dev Tutorial](https://concordant.io/tutorial)

## Components

The Concordant platform consists of different components depending on the deployement hierarchy level:

- [C-Client](https://github.com/concordant/c-client): Main local-first component. Designed to run in end-user devices; provides storage and sharing capabilities to applications at the Edge.
- [C-PoP](https://github.com/concordant/c-service): Designed to run in Point-of-Presence (PoP) devices at the edge of the network; provides nearby data access, storage and computation services for remote devices at the cloud-edge boundary.
- [C-Cloud](https://github.com/concordant/c-service): packaged to run in cloud infrastructures; provides the cloud based backend service for long-term data storage and processing.
- [C-Service](https://github.com/concordant/c-service): Concordant is not a self-contained database; it is a CRDT-style abstraction layer over other databases. By default, C-Client ships with the IndexedDB adapter for the browser, a LevelDB adapter in Node.js and HTTP/REST connector for CouchDB. The C-Service components contains the abstraction layer logic, with adapters and drivers depending on backend and access needed for the app.

*Note:* C-PoP and C-Cloud are currently part of the C-Service using external drivers as first backends, the ongoing developement focuses on C-Client.

### Libraries

- [C-CRDTLib](https://github.com/concordant/c-crdtlib): The Concordant Conflict-Free Replicated Datatypes (CRDT) library

### Demo apps and examples

- [React Markdown Editor](https://github.com/concordant/c-markdown-editor)
- [Collaborative Spreadsheet](https://github.com/itoumlilt/CRDT-Spreasheet)
- [Sudoku Game](https://github.com/concordant/c-sudoku)
- [CRDT Demonstrator](https://github.com/concordant/c-sudoku)

### Documentation

- [C-CRDT Package](https://concordant.gitlabpages.inria.fr/software/c-crdtlib/c-crdtlib/)
- [C-Client API](https://concordant.gitlabpages.inria.fr/software/c-client/c-client/)

## Community Guidelines

This repo contains guidelines for participatins in the Concordant community:

- [Code of conduct](./CODE_OF_CONDUCT.md)
- [License](./LICENSE)
- [Contributing](./CONTRIBUTING.md)

If you have any questions or concerns, please use the Issues menu in Github, or contact us directly by email [support@concordant.io](mailto:support@concordant.io).
