# Upstream Policy

BeMyTube is not maintained as a traditional FreeTube fork.

FreeTube is kept as a vendored upstream reference under:

    vendor/Freetube-App/

The BeMyTube project root is reserved for Haiku-native code,
project documentation, provider abstractions, and integration layers.

## Policy

Do not merge upstream FreeTube branches directly into BeMyTube's
development branch.

FreeTube updates must be imported deliberately as reviewed code deltas.

## Update model

1. Inspect upstream FreeTube changes.
2. Identify relevant files or concepts.
3. Apply only the needed delta inside vendor/Freetube-App/ or the
   BeMyTube integration layer.
4. Keep Haiku-native code outside vendor/.
5. Do not edit vendored files casually.
6. Document imported deltas when they affect architecture or behavior.

## Rationale

The BeMyTube tree intentionally separates the Haiku-native application
from the FreeTube reference implementation. Direct upstream merges would
mix two different repository layouts and make future maintenance harder.
