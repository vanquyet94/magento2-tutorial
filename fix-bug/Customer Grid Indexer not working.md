I apologize because in the previous comment I indicated that the
Magento \ Customer \ Model \ Indexer \ Source.php file did not exist, while it is actually alive and well.

However, by modifying the indexer.xml file the index rebuilding work fine.

Alternativly is possible add the below function to the file Source.php:
~~~php
public function addAttributeToSelect($attribute, $joinType = false)
{
    $this->customerCollection->addAttributeToSelect($attribute, $joinType);
    return $this;
}
~~~
I tested both methods on my test site.