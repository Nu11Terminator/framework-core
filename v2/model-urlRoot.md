---
title: Model - urlRoot
---

# urlRoot
Use the urlRoot property to define the base location for the resource the model identifies.

The default implementation of the *url* method generates a URL in the form of `urlRoot/id`.

For example, if the *urlRoot* is set to `'/documents'` and the *id* is set to `'321YWCE_0000G4PHB000002'`, the default implementation of the *url* method returns `'documents/321YWCE_0000G4PHB000002'`.
