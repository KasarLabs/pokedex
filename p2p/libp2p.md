---
id: libp2p
title: LibP2P
next_page: p2p_deoxys
---

## Concepts clés

### Transports
Les transports sont des mécanismes qui permettent aux pairs libp2p d'établir des connexions réseau entre eux. libp2p supporte plusieurs types de transports comme TCP, UDP, WebSockets et même des transports personnalisés.

### Muxing
Le multiplexage de flux (ou muxing) permet d'avoir plusieurs flux de communication logiques sur une seule connexion physique. Cela optimise l'utilisation des ressources réseau, surtout dans les contextes où établir des connexions est coûteux ou limité. libp2p utilise des protocoles comme mplex ou yamux pour le multiplexage.

### NAT Traversal
Le NAT (Network Address Translation) peut empêcher les pairs derrière des routeurs ou des pare-feux de communiquer directement. libp2p fournit des mécanismes de NAT Traversal comme le Hole Punching ou l'utilisation de relais pour faciliter la communication entre ces pairs.

### Peer Routing
Le routage des pairs permet de découvrir et de se connecter à des pairs spécifiques dans le réseau libp2p. Des algorithmes de découverte de pairs comme Kademlia aident à localiser les pairs détenant des ressources spécifiques ou à diffuser des informations à travers le réseau.

### PubSub
Le système de publication/abonnement (PubSub) est un modèle de communication où les pairs peuvent publier des messages sur des sujets, et d'autres pairs abonnés à ces sujets reçoivent les messages. libp2p supporte des protocoles PubSub comme Gossipsub pour une diffusion efficace dans le réseau.

### Cryptography
La sécurité est essentielle dans les réseaux pair-à-pair. libp2p intègre la cryptographie pour sécuriser les communications, en utilisant des identités basées sur des clés publiques pour l'authentification des pairs et le chiffrement des données pour la confidentialité.

## Résumé

- transports
  - TCP
  - UDP
  - WebSockets
  - QUIC
- Protocoles de Sécurité
  - Noise
  - TLS
- Multiplexage (Muxing)
  - yamux
  - mplex
- NAT Traversal
  - UPnP
  - Hole Punching
- Découverte de Pairs
  - mDNS (Multicast DNS)
  - Kademlia (DHT)
- PubSub
  - Gossipsub
  - Floodsub
- Cryptographie
  - Identités (Clés Publiques/Privées)
  -  Echange de clés sécurisé