# Client full reference

## Fields

### Attributes

None.

### Protected

| Field name      | Default value | Type                 |
|-----------------|---------------|----------------------|
| config          | unset         | `array`              |
| defaultMerchant | `null`        | `array`              |
| defaultConfig   | see blow      | `array`              |
| client          | unset         | `\GuzzleHttp\Client` |

#### Default config

```php
[
    'timeout'     => 30,
    'base_uri'    => 'https://www.szamlazz.hu/',
    'certificate' => [
        'enabled' => false,
    ],
    'storage'     => [
        'auto_save' => false,
        'disk'      => 'local',
        'path'      => 'szamlazzhu',
    ],
];
```


## Methods

| Method name                        | Return one of these                                           | Parameters                                                                                                    |
|------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| getConfig()                        | `array`                                                       |                                                                                                               |
| validateReceiptForSaving()         | `bool`                                                        | `Receipt $receipt`                                                                                            |
| validateInvoiceForSaving()         | `bool`                                                        | `Invoice $invoice`                                                                                            |
| validateProformaInvoiceForSaving() | `bool`                                                        | `ProformaInvoice $invoice`                                                                                    |
| uploadProFormaInvoice()            | `InvoiceCreationResponse`                                     | `ProformaInvoice $invoice`,<br> `$withoutPdf = false`,<br> `$emailSubject = null`,<br> `$emailMessage = null` |
| uploadInvoice()                    | `InvoiceCreationResponse`                                     | `Invoice $invoice`,<br> `$withoutPdf = false`,<br> `$emailSubject = null`,<br> `$emailMessage = null`         |
| deleteProFormaInvoice()            | `ProformaInvoiceDeletionResponse`                             | `ProformaInvoice $invoice`                                                                                    |
| cancelInvoice()                    | `InvoiceCancellationResponse`                                 | `Invoice $invoice`,<br> `$withoutPdf = false`,<br> `$emailSubject = null`,<br> `$emailMessage = null`         |
| getInvoiceByOrderNumber()          | `Invoice`<br>`ProformaInvoice`<br>`AbstractInvoice`           | `$orderNumber`                                                                                                |
| getInvoiceByOrderNumberOrFail()    | `mixed`                                                       | `$orderNumber`                                                                                                |
| getInvoiceOrFail()                 | `AbstractInvoice`<br>`Invoice`<br>`ProformaInvoice`           | `$invoice`                                                                                                    |
| getInvoice()                       | `null`<br>`AbstractInvoice`<br>`Invoice`<br>`ProformaInvoice` | `$invoice`                                                                                                    |
| getProformaInvoiceOrFail()         | `AbstractInvoice`<br>`Invoice`<br>`ProformaInvoice`           | `$invoice`                                                                                                    |
| getProformaInvoice()               | `null`<br>`ProformaInvoice`                                   | `$invoice`                                                                                                    |
| uploadReceipt()                    | `ReceiptCreationResponse`                                     | `Receipt $receipt`,<br> `$withoutPdf = false`                                                                 |
| cancelReceipt()                    | `ReceiptCancellationResponse`                                 | `Receipt $receipt`,<br> `$withoutPdf = false`                                                                 |
| getReceipt()                       | `Receipt`<br>`null`                                           | `Receipt $receipt`,<br> `$withoutPdf = false`                                                                 |
| getReceiptOrFail()                 | `Receipt`                                                     | `Receipt $receipt`,<br> `$withoutPdf = false`                                                                 |
| getReceiptByReceiptNumber()        | `Receipt`<br>`null`                                           | `$receiptNumber`,<br> `$withoutPdf = false`                                                                   |
| getReceiptByReceiptNumberOrFail()  | `Receipt`                                                     | `$receiptNumber`,<br> `$withoutPdf = false`                                                                   |
