Load a joomla module in an external php page

```php
//On initialisise le framework de Joomla 
define('_JEXEC', 1);

if (file_exists(__DIR__ . '/defines.php'))
{
    include_once __DIR__ . '/defines.php';
}

if (!defined('_JDEFINES'))
{
    define('JPATH_BASE', __DIR__);
    require_once JPATH_BASE . '/includes/defines.php';
}

require_once JPATH_BASE . '/includes/framework.php';

$app = JFactory::getApplication('site');
$app->initialise();
```

```php
//Puis on appel la position ou le module 
echo JHtml::_('content.prepare', '{loadposition position-22}');
```

## Lien Module 

```php
// Déclaration en tête de fichier en dessus de define or die
$urls = json_decode($item->urls); 
// Remplace $item->link quand on veut bind le lien a vers le lire la suite 
(!empty($urls->urla)?$urls->urla:$item->link)
```
