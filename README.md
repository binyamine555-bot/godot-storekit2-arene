# godot-storekit2 (v0.2 + ajouts)

Copie de [godot-sdk-integrations/godot-storekit2](https://github.com/godot-sdk-integrations/godot-storekit2) v0.2 (licence MIT), pour Godot 4.5.2, avec trois ajouts :

- `transaction_state_changed` donne aussi `transaction_id`, `original_transaction_id`, `purchase_date` (unix) et `source` (`purchase`, `updates`, `unfinished`) ;
- les transactions ne sont plus terminées automatiquement : le jeu appelle `finish_transaction(transaction_id)` après avoir crédité (signal `transaction_finished`) ;
- `present_code_redemption_sheet()` ouvre la fenêtre Apple de saisie de code d'offre (iOS 16+, signal `code_redemption_sheet_closed`).

`arene_version()` renvoie `0.2-arene1`. Construit par GitHub Actions (macOS), résultat sur les branches `build-*`.
