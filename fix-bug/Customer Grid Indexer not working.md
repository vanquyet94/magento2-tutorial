Modifying the indexer.xml file the index rebuilding work fine.

Add the below function to the file Source.php:
>Magento\Customer\Model\Indexer\Source.php

~~~php
public function addAttributeToSelect($attribute, $joinType = false)
{
    $this->customerCollection->addAttributeToSelect($attribute, $joinType);
    return $this;
}
~~~
I tested both methods on my test site.
