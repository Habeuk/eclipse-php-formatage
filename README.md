# Eclipse PHP Formatter Profiles

Profils de formatage de code PHP pour Eclipse PDT.

## 📋 Profils disponibles

| Profil | Description |
|--------|-------------|
| **Drupal Coding Standard v2** | Basé sur les standards Drupal (indentation 2 espaces) |
| **Symfony 8** | Adapté pour Symfony 8 avec support PHP 8.4 (property hooks, groupes de sérialisation) |

## 🔧 Installation

1. Ouvrir Eclipse
2. `Window` → `Preferences` → `PHP` → `Code Style` → `Formatter`
3. Cliquer sur `Import...`
4. Sélectionner le fichier XML du profil souhaité
5. Appliquer

## 📝 Détails du profil Symfony 8

- Indentation : 2 espaces
- Accolades : sur la même ligne (K&R)
- Longueur de ligne : 200 caractères
- Support PHP 8.4 : property hooks, asymmetric visibility
- Attributs `#[Groups]` sur une seule ligne

## 📸 Aperçu

### Symfony 8
```php
#[Groups(['user:read', 'user:write', 'admin:read', 'admin:write'])]
public string $email {
  get => $this->email;
  set(string $value) {
    $this->email = trim($value);
  }
}
