---
id: p2p_deoxys
title: P2P Deoxys
prev_page: libp2p
---

## Mode de synchronisation

### feeder: *synchronisation directement depuis le sequencer feeder gateway*
1. connection au sequencer pour la recuperation de:
  - blocs
  - state update
  - classes
  - *(signature du block_hash & state_diff_commitment)*
2. vérification des blocs sur la L1
3. distribution aux pairs

### non-feeder: *synchronisation via les autres pairs P2P*
1. découverte du réseau via un noeud stable feeder*
2. recuperation de la clé public du sequencer
3. demande des composants de blocs à différents pairs
4. vérification des blocs:
  - *accepeted on L1*: vérification via le contrat L1
  - *accepted on L2*: vérification de la signature des blocs avec la clé publique
5. distribution aux pairs