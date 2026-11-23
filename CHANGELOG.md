All notable changes to this project will be documented in this section.

Version numbers are using **MAJOR**.**MINOR**.**PATCH** numbering format for example 1.2.34

**MAJOR** will be incremented only if there is an incompatible breaking change. New distinct documentation and specification files will be published.

**MINOR** will be incremented only if a function becomes deprecated or deleted (after being deprecated in a previous version)

**PATCH** will be incremented everytime changes and additions are released.

For each version, there will be the list of changes:
* **Breaking Changes** for breaking changes you need to take into consideration before updating.
* **Added** for new features.
* **Changed** for changes in existing functionality.
* **Deprecated** for soon-to-be removed features.
* **Removed** for now removed features.
* **Fixed** for any bug fixes.
* **Security** in case of vulnerabilities.

**Removal lifecycle**<br>
Once a function becomes **Deprecated**, we monitor its usage to track how many users are still using it.
After a long period of time, if a minority of users are still using the function, we might ask users to update to the newer version of the function and give them ample time to do so.
Only after that delay expires (or no more users are still using it), we will have the function **Removed**.

You can always safely update to newer **PATCH** version if you stay in the same **MAJOR**.**MINOR** prefix.

You can safely update to a newer **MINOR** version as long as you don't jump more than a version at a time.

## 1.3.X Releases

### ⚠️ Compatibility Warning

Starting with **version 1.3.0**, several API endpoints have been updated to support a **major enhancement**:
You can now **combine and alternate form steps and signature steps** within the same signing workflow.

This provides greater flexibility, but it also changes how **step numbers** are defined and managed.

* **Endpoints introduced in 1.3.0** (listed below) use the *new step numbering model*.
* **Endpoints from previous versions (≤ 1.2.2)** use the *old step numbering model*.
* These two models are **not compatible** — mixing old and new endpoints within the same implementation could cause inconsistencies.

You may continue using the old routes or migrate fully to the new ones, but **do not mix both** in a single integration.

### Endpoints with Step Numbers (pre-1.3.0)

* GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getActionableElements
* GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getCompletedElements
* GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignsignatures
* GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getActionableElements
* GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsigndocuments
* GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplatesignatures
* GET /2/object/ezsigndocument/{pkiEzsigndocumentID}
* GET /3/object/ezsignsignature/{pkiEzsignsignatureID}
* GET /3/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
* POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/createEzsignelementsPositionedByWord
* POST /1/object/ezsignfolder/{pkiEzsignfolderID}/importEzsigntemplatepackage
* POST /2/object/ezsigntemplatesignature
* POST /3/object/ezsignsignature
* PUT /1/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignformfieldgroups
* PUT /1/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignsignatures
* PUT /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/editEzsigntemplatesignatures
* PUT /2/object/ezsignsignature/{pkiEzsignsignatureID}
* PUT /2/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}

### Updated endpoints with Step Numbers (introduced in 1.3.0)

* GET /2/object/ezsigndocument/{pkiEzsigndocumentID}/getActionableElements
* GET /2/object/ezsigndocument/{pkiEzsigndocumentID}/getCompletedElements
* GET /2/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignsignatures
* GET /2/object/ezsignfolder/{pkiEzsignfolderID}/getActionableElements
* GET /2/object/ezsignfolder/{pkiEzsignfolderID}/getEzsigndocuments
* GET /2/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplatesignatures
* GET /3/object/ezsigndocument/{pkiEzsigndocumentID}
* GET /4/object/ezsignsignature/{pkiEzsignsignatureID}
* GET /4/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
* POST /2/object/ezsigndocument/{pkiEzsigndocumentID}/createEzsignelementsPositionedByWord
* POST /2/object/ezsignfolder/{pkiEzsignfolderID}/importEzsigntemplatepackage
* POST /3/object/ezsigntemplatesignature
* POST /4/object/ezsignsignature
* PUT /2/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignformfieldgroups
* PUT /2/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignsignatures
* PUT /2/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/editEzsigntemplatesignatures
* PUT /3/object/ezsignsignature/{pkiEzsignsignatureID}
* PUT /3/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}

---

### [1.3.4] - 2026-XX-XX

#### Added
- DELETE /1/object/documenttypechecklist/{pkiDocumenttypechecklistID}
- GET /1/object/adjustment/getList
- GET /1/object/adjustment/{pkiAdjustmentID}/getAttachments
- GET /1/object/adjustment/{pkiAdjustmentID}/getCommunicationCount
- GET /1/object/adjustment/{pkiAdjustmentID}/getCommunicationList
- GET /1/object/adjustment/{pkiAdjustmentID}/getCommunicationrecipients
- GET /1/object/adjustment/{pkiAdjustmentID}/getCommunicationsenders
- GET /1/object/adjustmentreminder/getList
- GET /1/object/agent/{pkiAgentID}/getAttachments
- GET /1/object/agent/{pkiAgentID}/getCommunicationCount
- GET /1/object/agent/{pkiAgentID}/getCommunicationList
- GET /1/object/agent/{pkiAgentID}/getCommunicationrecipients
- GET /1/object/agent/{pkiAgentID}/getCommunicationsenders
- GET /1/object/bankaccount/getList
- GET /1/object/bankaccount/{pkiBankaccountID}/getAttachments
- GET /1/object/bankaccount/{pkiBankaccountID}/getCommunicationCount
- GET /1/object/bankaccount/{pkiBankaccountID}/getCommunicationList
- GET /1/object/bankaccount/{pkiBankaccountID}/getCommunicationrecipients
- GET /1/object/bankaccount/{pkiBankaccountID}/getCommunicationsenders
- GET /1/object/broker/{pkiBrokerID}/getAttachments
- GET /1/object/broker/{pkiBrokerID}/getCommunicationCount
- GET /1/object/broker/{pkiBrokerID}/getCommunicationList
- GET /1/object/broker/{pkiBrokerID}/getCommunicationrecipients
- GET /1/object/broker/{pkiBrokerID}/getCommunicationsenders
- GET /1/object/buyercontract/{pkiBuyercontractID}/getAttachments
- GET /1/object/commissionadvance/{pkiCommissionadvanceID}/getAttachments
- GET /1/object/commissionadvance/{pkiCommissionadvanceID}/getCommunicationCount
- GET /1/object/commissionadvance/{pkiCommissionadvanceID}/getCommunicationList
- GET /1/object/commissionadvance/{pkiCommissionadvanceID}/getCommunicationrecipients
- GET /1/object/commissionadvance/{pkiCommissionadvanceID}/getCommunicationsenders
- GET /1/object/customer/{pkiCustomerID}/getAttachments
- GET /1/object/customer/{pkiCustomerID}/getCommunicationCount
- GET /1/object/customer/{pkiCustomerID}/getCommunicationList
- GET /1/object/customer/{pkiCustomerID}/getCommunicationrecipients
- GET /1/object/customer/{pkiCustomerID}/getCommunicationsenders
- GET /1/object/deposit/getList
- GET /1/object/deposit/{pkiDepositID}/getAttachments
- GET /1/object/deposit/{pkiDepositID}/getCommunicationCount
- GET /1/object/deposit/{pkiDepositID}/getCommunicationList
- GET /1/object/deposit/{pkiDepositID}/getCommunicationrecipients
- GET /1/object/deposit/{pkiDepositID}/getCommunicationsenders
- GET /1/object/deposittransitcheque/getList
- GET /1/object/deposittransitcheque/{pkiDeposittransitchequeID}/getAttachments
- GET /1/object/deposittransitcheque/{pkiDeposittransitchequeID}/getCommunicationCount
- GET /1/object/deposittransitcheque/{pkiDeposittransitchequeID}/getCommunicationList
- GET /1/object/deposittransitcheque/{pkiDeposittransitchequeID}/getCommunicationrecipients
- GET /1/object/deposittransitcheque/{pkiDeposittransitchequeID}/getCommunicationsenders
- GET /1/object/disclosure/getList
- GET /1/object/disclosure/{pkiDisclosureID}/getAttachments
- GET /1/object/disclosure/{pkiDisclosureID}/getCommunicationCount
- GET /1/object/disclosure/{pkiDisclosureID}/getCommunicationList
- GET /1/object/disclosure/{pkiDisclosureID}/getCommunicationrecipients
- GET /1/object/disclosure/{pkiDisclosureID}/getCommunicationsenders
- GET /1/object/documenttype/getList
- GET /1/object/electronicfundstransfer/getList
- GET /1/object/electronicfundstransfer/{pkiElectronicfundstransferID}/getAttachments
- GET /1/object/electronicfundstransfertransaction/getList
- GET /1/object/employee/{pkiEmployeeID}/getAttachments
- GET /1/object/employee/{pkiEmployeeID}/getCommunicationCount
- GET /1/object/employee/{pkiEmployeeID}/getCommunicationList
- GET /1/object/employee/{pkiEmployeeID}/getCommunicationrecipients
- GET /1/object/employee/{pkiEmployeeID}/getCommunicationsenders
- GET /1/object/externalbroker/{pkiExternalbrokerID}/getAttachments
- GET /1/object/externalbroker/{pkiExternalbrokerID}/getCommunicationCount
- GET /1/object/externalbroker/{pkiExternalbrokerID}/getCommunicationList
- GET /1/object/externalbroker/{pkiExternalbrokerID}/getCommunicationrecipients
- GET /1/object/externalbroker/{pkiExternalbrokerID}/getCommunicationsenders
- GET /1/object/folder/{pkiFolderID}/getAttachments
- GET /1/object/folder/{pkiFolderID}/getCommunicationCount
- GET /1/object/folder/{pkiFolderID}/getCommunicationList
- GET /1/object/folder/{pkiFolderID}/getCommunicationrecipients
- GET /1/object/folder/{pkiFolderID}/getCommunicationsenders
- GET /1/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}/getAttachments
- GET /1/object/inscriptiontemp/{pkiInscriptiontempID}/getAttachments
- GET /1/object/invoice/getList
- GET /1/object/lead/{pkiLeadID}/getAttachments
- GET /1/object/lead/{pkiLeadID}/getCommunicationCount
- GET /1/object/lead/{pkiLeadID}/getCommunicationList
- GET /1/object/lead/{pkiLeadID}/getCommunicationrecipients
- GET /1/object/lead/{pkiLeadID}/getCommunicationsenders
- GET /1/object/notary/getList
- GET /1/object/notary/{pkiNotaryID}/getAttachments
- GET /1/object/notary/{pkiNotaryID}/getCommunicationCount
- GET /1/object/notary/{pkiNotaryID}/getCommunicationList
- GET /1/object/notary/{pkiNotaryID}/getCommunicationrecipients
- GET /1/object/notary/{pkiNotaryID}/getCommunicationsenders
- GET /1/object/officetaxreport/getList
- GET /1/object/officetaxreport/{pkiOfficetaxreportID}/getAttachments
- GET /1/object/officetaxreport/{pkiOfficetaxreportID}/getCommunicationCount
- GET /1/object/officetaxreport/{pkiOfficetaxreportID}/getCommunicationList
- GET /1/object/officetaxreport/{pkiOfficetaxreportID}/getCommunicationrecipients
- GET /1/object/officetaxreport/{pkiOfficetaxreportID}/getCommunicationsenders
- GET /1/object/otherincome/{pkiOtherincomeID}/getAttachments
- GET /1/object/paymentpreparation/{pkiPaymentpreparationID}/getAttachments
- GET /1/object/paymentpreparation/{pkiPaymentpreparationID}/getCommunicationCount
- GET /1/object/paymentpreparation/{pkiPaymentpreparationID}/getCommunicationList
- GET /1/object/paymentpreparation/{pkiPaymentpreparationID}/getCommunicationrecipients
- GET /1/object/paymentpreparation/{pkiPaymentpreparationID}/getCommunicationsenders
- GET /1/object/purchase/getList
- GET /1/object/purchase/{pkiPurchaseID}/getAttachments
- GET /1/object/purchase/{pkiPurchaseID}/getCommunicationCount
- GET /1/object/purchase/{pkiPurchaseID}/getCommunicationList
- GET /1/object/purchase/{pkiPurchaseID}/getCommunicationrecipients
- GET /1/object/purchase/{pkiPurchaseID}/getCommunicationsenders
- GET /1/object/reconciliation/{pkiReconciliationID}/getAttachments
- GET /1/object/reconciliation/{pkiReconciliationID}/getCommunicationCount
- GET /1/object/reconciliation/{pkiReconciliationID}/getCommunicationList
- GET /1/object/reconciliation/{pkiReconciliationID}/getCommunicationrecipients
- GET /1/object/reconciliation/{pkiReconciliationID}/getCommunicationsenders
- GET /1/object/rejectedoffertopurchase/{pkiRejectedoffertopurchaseID}/getAttachments
- GET /1/object/salary/getList
- GET /1/object/salary/{pkiSalaryID}/getAttachments
- GET /1/object/salary/{pkiSalaryID}/getCommunicationCount
- GET /1/object/salary/{pkiSalaryID}/getCommunicationList
- GET /1/object/salary/{pkiSalaryID}/getCommunicationrecipients
- GET /1/object/salary/{pkiSalaryID}/getCommunicationsenders
- GET /1/object/supplier/{pkiSupplierID}/getAttachments
- GET /1/object/supplier/{pkiSupplierID}/getCommunicationCount
- GET /1/object/supplier/{pkiSupplierID}/getCommunicationList
- GET /1/object/supplier/{pkiSupplierID}/getCommunicationrecipients
- GET /1/object/supplier/{pkiSupplierID}/getCommunicationsenders
- GET /2/module/ezsign/suggestTemplates
- GET /2/object/attachmentrejectreason/getAutocomplete/{sSelector}
- GET /2/object/documenttype/getAutocomplete/{sSelector}
- GET /2/object/documenttype/{pkiDocumenttypeID}
- GET /3/object/ezsignbulksenddocumentmapping/{pkiEzsignbulksenddocumentmappingID}
- GET /3/object/ezsignbulksendsignermapping/{pkiEzsignbulksendsignermappingID}
- GET /3/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}
- GET /3/object/ezsigntemplatepackagemembership/{pkiEzsigntemplatepackagemembershipID}
- GET /3/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- GET /3/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- GET /4/object/ezsignbulksend/{pkiEzsignbulksendID}
- GET /4/object/ezsigntemplate/{pkiEzsigntemplateID}
- PATCH /1/object/documenttypechecklist/{pkiDocumenttypechecklistID}
- POST /1/object/adjustment/{pkiAdjustmentID}/batchDownload
- POST /1/object/adjustment/{pkiAdjustmentID}/importIntoEDM
- POST /1/object/agent/{pkiAgentID}/batchDownload
- POST /1/object/attachment/{pkiAttachmentID}/delete
- POST /1/object/attachment/{pkiAttachmentID}/rename
- POST /1/object/attachment/{pkiAttachmentID}/restore
- POST /1/object/attachment/{pkiAttachmentID}/setDocumentType
- POST /1/object/attachment/{pkiAttachmentID}/setPrivacy
- POST /1/object/attachment/{pkiAttachmentID}/validate
- POST /1/object/bankaccount/{pkiBankaccountID}/batchDownload
- POST /1/object/bankaccount/{pkiBankaccountID}/importIntoEDM
- POST /1/object/broker/{pkiBrokerID}/batchDownload
- POST /1/object/buyercontract/{pkiBuyercontractID}/batchDownload
- POST /1/object/commissionadvance/{pkiCommissionadvanceID}/batchDownload
- POST /1/object/commissionadvance/{pkiCommissionadvanceID}/importIntoEDM
- POST /1/object/customer/{pkiCustomerID}/batchDownload
- POST /1/object/deposit/{pkiDepositID}/batchDownload
- POST /1/object/deposit/{pkiDepositID}/importIntoEDM
- POST /1/object/deposittransitcheque/{pkiDeposittransitchequeID}/batchDownload
- POST /1/object/deposittransitcheque/{pkiDeposittransitchequeID}/importIntoEDM
- POST /1/object/disclosure/{pkiDisclosureID}/batchDownload
- POST /1/object/disclosure/{pkiDisclosureID}/importIntoEDM
- POST /1/object/documenttype
- POST /1/object/electronicfundstransfer/{pkiElectronicfundstransferID}/batchDownload
- POST /1/object/employee/{pkiEmployeeID}/batchDownload
- POST /1/object/externalbroker/{pkiExternalbrokerID}/batchDownload
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/batchDownload
- POST /1/object/folder/{pkiFolderID}/batchDownload
- POST /1/object/folder/{pkiFolderID}/importIntoEDM
- POST /1/object/inscription/{pkiInscriptionID}/batchDownload
- POST /1/object/inscription/{pkiInscriptionID}/synchronizationDocumenttype
- POST /1/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}/batchDownload
- POST /1/object/inscriptiontemp/{pkiInscriptiontempID}/batchDownload
- POST /1/object/invoice/{pkiInvoiceID}/batchDownload
- POST /1/object/lead/{pkiLeadID}/batchDownload
- POST /1/object/notary/{pkiNotaryID}/batchDownload
- POST /1/object/notary/{pkiNotaryID}/importIntoEDM
- POST /1/object/officetaxreport/{pkiOfficetaxreportID}/batchDownload
- POST /1/object/officetaxreport/{pkiOfficetaxreportID}/importIntoEDM
- POST /1/object/otherincome/{pkiOtherincomeID}/batchDownload
- POST /1/object/paymentpreparation/{pkiPaymentpreparationID}/batchDownload
- POST /1/object/paymentpreparation/{pkiPaymentpreparationID}/importIntoEDM
- POST /1/object/purchase/{pkiPurchaseID}/batchDownload
- POST /1/object/purchase/{pkiPurchaseID}/importIntoEDM
- POST /1/object/reconciliation/{pkiReconciliationID}/batchDownload
- POST /1/object/reconciliation/{pkiReconciliationID}/importIntoEDM
- POST /1/object/rejectedoffertopurchase/{pkiRejectedoffertopurchaseID}/batchDownload
- POST /1/object/salary/{pkiSalaryID}/batchDownload
- POST /1/object/salary/{pkiSalaryID}/importIntoEDM
- POST /1/object/supplier/{pkiSupplierID}/batchDownload
- POST /2/object/ezsignbulksendsignermapping
- POST /2/object/ezsigntemplatepackagesigner
- POST /2/object/ezsigntemplatesigner
- PUT /1/object/documenttype/{pkiDocumenttypeID}
- PUT /2/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}/editEzsigntemplatepackagesigners
- PUT /2/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- PUT /2/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- Selector AttachmentSpecificUser in GET /2/object/user/getAutocomplete/{sSelector}
- Selector Required in GET /3/object/inscriptionchecklist/getAutocomplete/{sSelector}
- Parameter fkiAttachmentID in GET /2/object/user/getAutocomplete/{sSelector}
- Property dtAgentPermitexpiration in agent-ListElement
- Property dtEzsignformfieldgroupCompleted in ezsignformfieldgroup-Response
- Property eEzmaxcaseGooddaytaskstatus in ezmaxcase-Response and ezmaxcase-Listelement
- Property eEzsignfoldersignerassociationRole in ezsignfoldersignerassociation-RequestPatch
- Property fkiAgentID in user-ListElement
- Property fkiBrokerID in user-ListElement
- Property sAttachmentCategory in attachment-Response
- Property objCreditcardmerchant in ezsignsignature-ResponseCompound
- Property objUserSpecific in attachment-Response
- Property eWebhookEzmaxpartnerevent in webhook-sendWebhook-v1-Request
- Property sUserLoginname in Custom-UserName-Response
- Property fkiCompanyID in activesession-Response
- Property fkiDepartmentID in activesession-Response
- Property fkiDocumenttypechecklistID in attachment-Response
- Property sDocumenttypeNameX in attachment-Response
- Property objUser in attachmentlog-Response
- Property bKeepenteredvalues in ezsignfolder-duplicate-v1-Request
- Property fkiInscriptionnotauthenticatedID in communicationreference-Request
- Property objInscription in inscriptionnotauthenticated-Response
- Property bListpresentationCount in listpresentation-Request
- Property bListpresentationPinned in listpresentation-Request
- Enum value 'Optional' for Field-eEzsigntemplatesignatureConsultationtrigger
- Enum value 'CCDeleted' for Field-eEzsignfoldersignerassociationRole
- Enum value 'BuyercontractCreated' for Field-eWebhookRealestateevent
- Enum value 'BuyercontractModified' for Field-eWebhookRealestateevent
- Enum value 'CONFLICT' for Field-eErrorCode
- Enum value 'Pending' for Field-eAttachmentVerified
- Enum value 'Pending' for Field-eAttachmentlogType
- Enum value 'Realestate' for Field-eEzmaxpartnerproductstagewebhookModule
- Enum value 'SubactionEDM' for Field-ePathAction
- Webhook Buyercontract BuyercontractCreated
- Webhook Buyercontract BuyercontractModified

### [1.3.3] - 2026-07-22

#### Fixed
- Minor structural changes

### [1.3.2] - 2026-07-21

#### Added
- GET /2/module/ezsign/suggestSigners
- GET /2/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignfoldersignerassociations
- GET /3/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- GET /2/object/inscription/{pkiInscriptionID}
- GET /1/object/inscription/{pkiInscriptionID}/getInscriptionnotauthenticateds
- GET /2/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}
- POST /2/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- POST /3/object/ezsignfoldersignerassociation
- Enum value 'Realestate' for eWebhookModule
- Properties pkiInscriptionbuildingtypeID, sInscriptionbuildingtypeNameX, pkiInscriptioncategoryID, sInscriptioncategoryNameX, iInscriptionUnit in inscription-Listelement
- Properties pkiInscriptionbuildingtypeID, sInscriptionbuildingtypeNameX, pkiInscriptioncategoryID, sInscriptioncategoryNameX, iInscriptionUnit in inscriptionnotauthenticated-Listelement
- Property eAgentSchedule in agent-ListElement
- Property bInscriptionnotauthenticatedDraft in inscriptionnotauthenticated-ListElement
- Webhook Realestate InscriptionCreated
- Webhook Realestate InscriptionModified
- Webhook Realestate InscriptionnotauthenticatedCreated
- Webhook Realestate InscriptionnotauthenticatedModified

### [1.3.1] - 2026-06-17

#### Added
- DELETE /1/object/ezsigntemplateannotation/{pkiEzsigntemplateannotationID}
- GET /1/object/ezmaxpartnerproductstage/{pkiEzmaxpartnerproductstageID}/getEzmaxpartnerproductstagepermissions
- GET /1/object/ezmaxpartnerproductstage/{pkiEzmaxpartnerproductstageID}/getEzmaxpartnerproductstagewebhooks
- GET /1/object/ezmaxmaillinglist/getList
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getActionableElementsForSigner
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplateannotations
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/duplicate
- POST /1/object/ezsigntemplateannotation
- POST /4/object/ezsignfoldertype
- PUT /1/object/ezsigntemplateannotation/{pkiEzsigntemplateannotationID}
- PUT /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/editEzsigntemplateannotations
- PUT /4/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getActionableElementsForSigner
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignannotations
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignformfieldgroups
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignsignatures
- GET /2/object/ezsigntemplateannotation/{pkiEzsigntemplateannotationID}
- GET /2/object/ezsigntemplateglobalannotation/{pkiEzsigntemplateglobalannotationID}
- POST /1/module/ezmaxmaillinglist/subscribe
- POST /2/object/ezsigndocument/{pkiEzsigndocumentID}/applyEzsigntemplateglobal
- POST /3/object/ezsigndocument/{pkiEzsigndocumentID}/applyEzsigntemplate
- POST /3/object/ezsignfolder/{pkiEzsignfolderID}/importEzsigntemplatepackage
- Selector AgentBrokerEmployeeEzsignUserNormal in GET /2/object/user/getAutocomplete/{sSelector}
- Properties dtAgentContractdate, dtAgentTransferdate, dtAgentSenioritydate, dtAgentSickleavestart and dtAgentSickleaveend in agent-ListElement
- Properties fkiCountryID and fkiProvinceID in agent-ListElement, broker-ListElement, customer-ListElement, employee-ListElement, inscription-ListElement, inscriptionnotauthenticated-ListElement, rejectedoffertopurchase-ListElement and supplier-ListElement
- Properties fkiEzsignbulksendID, sEzsignbulksendDescription, fkiEzsignbulksendtransmissionID, sEzsignbulksendtransmissionDescription, fkiEzsigntemplatepublicID, sEzsigntemplatepublicDescription, eEzsignfolderSource in object ezsignfolder-ListElement
- Properties bEzsignfoldertypeSenddocumentmergetoemail, bEzsignfoldertypeSenddocumentmergetoezsignsigner, bEzsignfoldertypeSenddocumentmergetoreceivealldocument and bEzsignfoldertypeSenddocumentmergetouser in ezsignfoldertype-RequestV3 and ezsignfoldertype-ResponseV4
- Property a_objEzsigntemplateannotation in ezsigntemplate-ResponseCompound
- Property a_objEzsigntemplateannotation in ezsigntemplate-ResponseCompoundV3
- Property a_objEzsigntemplateglobalannotation in ezsigntemplateglobal-ResponseCompound
- Property fkiEzmaxpartnerID in user-Response
- Property fkiEzmaxpartnerproductstageID in apikey-ResponseCompound
- Property iEzsignfolderStepcurrent in ezsignfolder-ResponseV3
- Property iEzsignfoldertypeArchivaldays in ezsignfoldertype-getDefaults-v2-Response-mPayload
- Property sBuyercontractContract in buyercontract-ListElement
- Property objInscription in inscriptionnotauthenticated-Response
- Value Optional in Field-eEzsignsignatureConsultationtrigger
- Value Suspended in Field-eSessionhistoryEndby

### [1.3.0] - 2026-01-24

#### Added
- GET /1/object/agent/getList
- GET /1/object/broker/getList
- GET /1/object/buyercontract/getList
- GET /1/object/customer/getList
- GET /1/object/employee/getList
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}/getBatchFile
- GET /1/object/ezsignbulksendtransmission/{pkiEzsignbulksendtransmissionID}/getBatchFile
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/download
- GET /1/object/inscriptiontemp/getList
- GET /1/object/lead/getList
- GET /1/object/otherincome/getList
- GET /1/object/rejectedoffertopurchase/getList
- GET /1/object/supplier/getList
- GET /2/object/agent/getAutocomplete/{sSelector}
- GET /2/object/agenttype/getAutocomplete/{sSelector}
- GET /2/object/broker/getAutocomplete/{sSelector}
- GET /2/object/brokertype/getAutocomplete/{sSelector}
- GET /2/object/ezsigndocument/{pkiEzsigndocumentID}/getActionableElements
- GET /2/object/ezsigndocument/{pkiEzsigndocumentID}/getCompletedElements
- GET /2/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignsignatures
- GET /2/object/ezsignfolder/{pkiEzsignfolderID}/getActionableElements
- GET /2/object/ezsignfolder/{pkiEzsignfolderID}/getEzsigndocuments
- GET /2/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplatesignatures
- GET /2/object/inscriptionchecklist/getAutocomplete/{sSelector}
- GET /2/object/leadsource/getAutocomplete/{sSelector}
- GET /2/object/notificationtest/{pkiNotificationtestID}/getElements
- GET /2/object/otherincometype/getAutocomplete/{sSelector}
- GET /2/object/paymentmethod/getAutocomplete/{sSelector}
- GET /3/object/ezsigndocument/{pkiEzsigndocumentID}
- GET /3/object/ezsigndocument/{pkiEzsigndocumentID}/getActionableElements
- GET /3/object/ezsignfolder/{pkiEzsignfolderID}/getActionableElements
- GET /4/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /4/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- POST /1/module/ezmaxcustomer/createCustomer
- POST /1/object/activesession/setGoal
- POST /1/object/agent/{pkiAgentID}/importIntoEDM
- POST /1/object/broker/{pkiBrokerID}/importIntoEDM
- POST /1/object/buyercontract/{pkiBuyercontractID}/importIntoEDM
- POST /1/object/customer/{pkiCustomerID}/importIntoEDM
- POST /1/object/electronicfundstransfer/{pkiElectronicfundstransferID}/importIntoEDM
- POST /1/object/employee/{pkiEmployeeID}/importIntoEDM
- POST /1/object/externalbroker/{pkiExternalbrokerID}/importIntoEDM
- POST /1/object/inscription/{pkiInscriptionID}/importIntoEDM
- POST /1/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}/importIntoEDM
- POST /1/object/inscriptiontemp/{pkiInscriptiontempID}/importIntoEDM
- POST /1/object/invoice/{pkiInvoiceID}/importIntoEDM
- POST /1/object/lead/{pkiLeadID}/importIntoEDM
- POST /1/object/otherincome/{pkiOtherincomeID}/importIntoEDM
- POST /1/object/rejectedoffertopurchase/{pkiRejectedoffertopurchaseID}/importIntoEDM
- POST /1/object/supplier/{pkiSupplierID}/importIntoEDM
- POST /1/object/tranqcontract/{pkiTranqcontractID}/importIntoEDM
- POST /1/report/accountspayable/accountspayable
- POST /1/report/accountsreceivablevscommission/accountsreceivablevscommission
- POST /2/object/ezsigndocument/{pkiEzsigndocumentID}/createEzsignelementsPositionedByWord
- POST /2/object/ezsignfolder/{pkiEzsignfolderID}/importEzsigntemplatepackage
- POST /2/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}/createEmbeddedUrl
- POST /3/object/ezsigntemplatesignature
- POST /4/object/ezsignsignature
- PUT /2/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignformfieldgroups
- PUT /2/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignsignatures
- PUT /2/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/editEzsigntemplatesignatures
- PUT /3/object/ezsignsignature/{pkiEzsignsignatureID}
- PUT /3/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- Properties a_objContactPrivate, a_objContactShared in ezsign-suggestSigners-v1-Response-mPayload
- Properties bEzsignfoldertypeSendsignatureattachmentezsignsigner, bEzsignfoldertypeSendsignatureattachment, bEzsignfoldertypeSendsignatureattachmentuser, bEzsignfoldertypeAllowdownloadsignatureattachmentezsignsigner, bEzsignfoldertypeSendsignatureattachmentreceivealldocument in ezsignfoldertype-RequestV3 and- ezsignfoldertype-ResponseV4
- Properties eEzsignsignatureSignaturepadrequired, eEzsignsignatureSignaturepadrequired in ezsignsignature-Request and ezsignsignature-Response
- Properties eEzsigntemplatesignatureSignaturepadrequired, eEzsigntemplatesignatureSignaturepadrequired in ezsigntemplatesignature-Request and ezsigntemplatesignature-Response
- Property a_objEzsignsignaturepaymentdetail in ezsignsignature-RequestCompound
- Property a_objEzsigntemplatesignaturepaymentdetail in ezsigntemplatesignature-RequestCompound, ezsigntemplatesignature-RequestCompoundV2, ezsigntemplatesignature-ResponseCompoundV3
- Property bInscriptionInspection in inscription-ListElement
- Property bInscriptionInspection in inscriptionnotauthenticated-ListElement
- Property bInscriptionnotauthenticatedConditional in inscription-ListElement
- Property bInscriptionnotauthenticatedConditional in inscriptionnotauthenticated-ListElement
- Property bUserAddmeinezsignfolder in activesession-ResponseCompound-User
- Property bUserAddmeinezsignfolder in user-getPreferences-v1-Response
- Property bUserAddmeinezsignfolder in user-setPreferences-v1-Request
- Property dtUserNpsrequest in activesession-ResponseCompound
- Property eEzsignfolderCompletion in ezsignfolder-ListElement
- Property eEzsignfolderDocumentmerge in ezsignfoldertype-RequestV3 and ezsignfoldertype-ResponseV4
- Property eEzsignfolderMessageorder in ezsignfolder-Response
- Property eUserType in ezsignfoldersignerassociation-ResponseCompound-User
- Property fkiDepartmentID in agent-AutocompleteElement-Response
- Property fkiDepartmentID in broker-AutocompleteElement-Response
- Property fkiDepartmentID in customer-AutocompleteElement-Response
- Property fkiEzsigntemplateglobalID in Custom-Ezsignimportdocument-Response
- Property fkiModuleIDForm in user-getPreferences-v1-Response-mPayload
- Property fkiModuleIDForm in user-setPreferences-v1-Request
- Property fkiPaymentgatewayID in ezsignsignature-Response, ezsigntemplatesignature-Request, ezsigntemplatesignature-Response
- Property iUserFrontendgoal in activesession-ResponseCompound-User
- Property iSystemconfigurationEzsignreminderhoursend in systemconfiguration-Request and systemconfiguration-Response
- Property objReportcellstyleCustom in Common-Reportrow
- Property sEzsignsignergroupDescriptionX in Custom-EzsignfoldertransmissionSigner-Response
- Property sEzsigntemplateglobalDescription in Custom-Ezsignimportdocument-Response
- Property sCustomerCode in customer-AutocompleteElement-Response
- Property sModuleNameX in user-getPreferences-v1-Response-mPayload
- Property sReportsectionTabname in Common-Reportsection
- Property sWebhookAuthentificationexternalerror in webhook-ResponseCompound
- Selector EzsignfoldertypeReassign in /2/object/userlogintype/getAutocomplete/{sSelector}
- Value PerEzsignfolderStepSync in eEzsignfolderCompletion
- Value PerEzsignfolderStepSync in eEzsignfoldertypeCompletion
- Value PendingPrematurelyEnded in eEzsigndocumentStep

#### Deprecated
- POST /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}/createEmbeddedUrl

#### Removed
- Property bEzsignfolderPaymentused in Custom-EzmaxinvoicingEzsignfolder-Response
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsigndocuments
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplatesignatures
- GET /1/object/notificationtest/{pkiNotificationtestID}/getElements
- GET /2/object/inscriptionchecklist/getAutocomplete
- GET /2/object/signature/{pkiSignatureID}
- GET /3/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /3/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID} 
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/reorder
- POST /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}/createEmbeddedUrl
- PUT /1/object/ezsignbulksend/{pkiEzsignbulksendID}
- PUT /1/object/systemconfiguration/{pkiSystemconfigurationID}
- PUT /2/object/ezsignsignature/{pkiEzsignsignatureID}
- PUT /2/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}

---

## 1.2.X Releases

### [1.2.2] - 2025-03-07

#### Added
- DELETE /1/object/ezsignimportfolder/{pkiEzsignimportfolderID}
- DELETE /1/object/ezsigntemplatepublic/{pkiEzsigntemplatepublicID}
- GET /1/module/user/getKeys
- GET /1/object/currency/getAutocomplete/{sSelector}
- GET /2/object/customer/getAutocomplete/{sSelector}
- GET /1/object/ezsignimportdocument/{pkiEzsignimportdocumentID}/download
- GET /1/object/ezsignimportfolder/getList
- GET /1/object/paymentgateway/{pkiPaymentgatewayID}
- GET /1/object/paymentgateway/getAutocomplete
- GET /1/object/paymentgateway/getList
- GET /2/object/ezsignimportfolder/{pkiEzsignimportfolderID}
- POST /1/module/user/generateKey
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/prefillEzsignform
- POST /1/object/paymentgateway
- PUT /1/object/paymentgateway/{pkiPaymentgatewayID}
- Property a_objReportgroupParameter in Common-Reportgroup
- Property a_sVariableobjectProperty in Common-Reportsubsectionpart
- Property bReportPaginate in Common-Report
- Property dtEzsignfolderArchive in ezsignfolder-ResponseV3
- Property dtEzsignfolderDispose in ezsignfolder-ResponseV3
- Property dtEzsignfolderArchive in ezsignfolder-ListElement
- Property dtEzsignfolderClose in ezsignfolder-ListElement
- Property dtEzsignfolderDispose in ezsignfolder-ListElement
- Property eReportcolumnType in Common-Reportcolumn
- Property iReportcellColumn in Common-Reportcell
- Property fkiEzsignimportdocumentID in ezsigndocument-Request
- Property sEzsignsignergroupDescriptionX in ezsignsignature-ResponseCompound
- Property sEzsignsignergroupDescriptionX in ezsignsignature-ResponseCompoundV3
- Property sReportgroupFilename in Common-Reportgroup
- Property sReportsectionTitle in Common-Reportsection
- Property sReportsubsectionTitle in Common-Reportsubsection
- Property sReportTitle in Common-Report
- Property objEzsignfoldertype in ezsigntemplate-ResponseV3
- Property objVariableobject in Common-Reportrow
- Value Ezsignimportdocument in eEzsigndocumentSource

### [1.2.1] - 2025-01-28

#### Notes
- The eZmax-SDK-csharp sdk can now be installed from NuGet

#### Added
- DELETE /1/object/authenticationexternal/{pkiAuthenticationexternalID}
- DELETE /1/object/creditcardmerchant/{pkiCreditcardmerchantID}
- DELETE /1/object/domain/{pkiDomainID}
- DELETE /1/object/ezsigntemplatedocumentpagerecognition/{pkiEzsigntemplatedocumentpagerecognitionID}
- DELETE /1/object/supply/{pkiSupplyID}
- GET /1/object/authenticationexternal/getList
- GET /1/object/buyercontract/{pkiBuyercontractID}/getCommunicationCount
- GET /1/object/buyercontract/{pkiBuyercontractID}/getCommunicationRecipients
- GET /1/object/buyercontract/{pkiBuyercontractID}/getCommunicationSenders
- GET /1/object/creditcardmerchant/getList
- GET /1/object/domain/getList
- GET /1/object/electronicfundstransfer/{pkiElectronicfundstransferID}/getCommunicationCount
- GET /1/object/electronicfundstransfer/{pkiElectronicfundstransferID}/getCommunicationRecipients
- GET /1/object/electronicfundstransfer/{pkiElectronicfundstransferID}/getCommunicationSenders
- GET /1/object/ezdoctemplatedocument/{pkiEzdoctemplatedocumentID}/download
- GET /1/object/ezdoctemplatedocument/getList
- GET /1/object/ezsigntemplatepublic/getList
- GET /1/object/ezsigntemplatepublic/getFormsData
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplatedocumentpagerecognitions
- GET /1/object/inscription/{pkiInscriptionID}/getCommunicationCount
- GET /1/object/inscription/{pkiInscriptionID}/getCommunicationRecipients
- GET /1/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}/getCommunicationCount
- GET /1/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}/getCommunicationRecipients
- GET /1/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}/getCommunicationSenders
- GET /1/object/invoice/{pkiInvoiceID}/getCommunicationCount
- GET /1/object/invoice/{pkiInvoiceID}/getCommunicationRecipients
- GET /1/object/invoice/{pkiInvoiceID}/getCommunicationSenders
- GET /1/object/otherincome/{pkiOtherincomeID}/getCommunicationCount
- GET /1/object/otherincome/{pkiOtherincomeID}/getCommunicationRecipients
- GET /1/object/otherincome/{pkiOtherincomeID}/getCommunicationSenders
- GET /1/object/rejectedoffertopurchase/{pkiRejectedoffertopurchaseID}/getCommunicationCount
- GET /1/object/rejectedoffertopurchase/{pkiRejectedoffertopurchaseID}/getCommunicationRecipients
- GET /1/object/rejectedoffertopurchase/{pkiRejectedoffertopurchaseID}/getCommunicationSenders
- GET /1/object/inscriptiontemp/{pkiInscriptiontempID}/getCommunicationCount
- GET /1/object/inscriptiontemp/{pkiInscriptiontempID}/getCommunicationRecipients
- GET /1/object/inscriptiontemp/{pkiInscriptiontempID}/getCommunicationSenders
- GET /1/object/signature/{pkiSignatureID}/getSVGInitials
- GET /1/object/signature/{pkiSignatureID}/getSVGSignature
- GET /1/object/supply/getList
- GET /1/object/tranqcontract/{pkiTranqcontractID}/getCommunicationCount
- GET /1/object/tranqcontract/{pkiTranqcontractID}/getCommunicationList
- GET /1/object/tranqcontract/{pkiTranqcontractID}/getCommunicationRecipients
- GET /1/object/tranqcontract/{pkiTranqcontractID}/getCommunicationSenders
- GET /1/object/user/{pkiUserID}/getColleagues
- GET /2/object/authenticationexternal/{pkiAuthenticationexternalID}
- GET /2/object/authenticationexternal/getAutocomplete/{sSelector}
- GET /2/object/bankaccount/getAutocomplete/{sSelector}
- GET /2/object/contacttitle/getAutocomplete/{sSelector}
- GET /2/object/creditcardmerchant/{pkiCreditcardmerchantID}
- GET /2/object/creditcardmerchant/getAutocomplete/{sSelector}
- GET /2/object/domain/{pkiDomainID}
- GET /2/object/ezdoctemplatedocument/{pkiEzdoctemplatedocumentID}
- GET /2/object/ezsignfoldertype/{pkiEzsignfoldertypeID}/getDefaults
- GET /2/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}
- GET /2/object/ezdoctemplatedocument/getAutocomplete/{sSelector}
- GET /2/object/ezsigntemplatedocumentpagerecognition/{pkiEzsigntemplatedocumentpagerecognitionID}
- GET /2/object/ezsignuser/{pkiEzsignuserID}
- GET /2/object/ezdoctemplatefieldtypecategory/getAutocomplete/{sSelector}
- GET /2/object/ezdoctemplatetype/getAutocomplete/{sSelector}
- GET /2/object/glaccount/getAutocomplete/{sSelector}
- GET /2/object/glaccountcontainer/getAutocomplete/{sSelector}
- GET /2/object/pdfalevel/getAutocomplete/{sSelector}
- GET /2/object/supply/{pkiSupplyID}
- GET /2/object/supply/getAutocomplete/{sSelector}
- GET /2/object/user/{pkiUserID}/getColleagues
- GET /3/object/ezsignfolder/{pkiEzsignfolderID}
- GET /3/object/branding/{pkiBrandingID}
- GET /3/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /3/object/ezsigntemplate/{pkiEzsigntemplateID}
- GET /3/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- GET /3/object/signature/{pkiSignatureID}
- GET /4/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- PATCH /1/object/creditcardclient/{pkiCreditcardclientID}
- POST /1/object/authenticationexternal
- POST /1/object/authenticationexternal/{pkiAuthenticationexternalID}/resetAuthorization
- POST /1/object/creditcardmerchant
- POST /1/object/domain
- POST /1/object/ezdoctemplatedocument
- POST /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}/reassign
- POST /1/object/ezsigntemplatefavorite/setFavorite
- POST /1/object/ezsigntemplatepublic
- POST /1/object/ezsigntemplatepublic/createEzsignfolder
- POST /1/object/ezsigntemplatepublic/getEzsigntemplatepublicDetails
- POST /1/object/ezsigntemplatepublic/resetUrl
- POST /1/object/ezsigntemplatepublic/resetLimitExceededCounter
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/extractText
- POST /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/extractText
- POST /1/object/ezsigntemplatedocumentpagerecognition
- POST /1/object/supply
- POST /1/object/webhook/sendWebhook
- POST /2/object/branding
- POST /2/object/ezsignbulksend/{pkiEzsignbulksendID}/createEzsignbulksendtransmission
- POST /2/object/ezsignfolder/{pkiEzsignfolderID}/reorder
- POST /2/object/ezsigntemplatesignature
- POST /3/object/ezsigndocument
- POST /3/object/ezsignfolder
- POST /3/object/ezsignfoldertype
- POST /3/object/ezsignsignature
- POST /3/object/ezsigntemplate
- PATCH /1/object/ezdoctemplatedocument/{pkiEzdoctemplatedocumentID}
- PUT /1/object/authenticationexternal/{pkiAuthenticationexternalID}
- PUT /1/object/creditcardmerchant/{pkiCreditcardmerchantID}
- PUT /1/object/ezdoctemplatedocument/{pkiEzdoctemplatedocumentID}
- PUT /2/object/ezsignsignature/{pkiEzsignsignatureID}
- PUT /1/object/ezsigntemplatepublic/{pkiEzsigntemplatepublicID}
- PUT /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/editEzsigntemplatedocumentpagerecognitions
- PUT /1/object/ezsigntemplatedocumentpagerecognition/{pkiEzsigntemplatedocumentpagerecognitionID}
- PUT /1/object/ezsignuser/{pkiEzsignuserID}
- PUT /1/object/supply/{pkiSupplyID}
- PUT /1/object/user/{pkiUserID}/editColleagues
- PUT /2/object/branding/{pkiBrandingID}
- PUT /2/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- PUT /2/object/user/{pkiUserID}/editColleagues
- PUT /3/object/ezsignfolder/{pkiEzsignfolderID}
- PUT /3/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- PUT /3/object/ezsigntemplate/{pkiEzsigntemplateID}
- Error code 403 FORBIDDEN_CLONE_PERMISSION
- Property a_objEzsigndocumentdependency in GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsigndocuments
- Multiple new properties in various objects for form field alignment, webhook configuration, font management, and more

#### Removed
- GET /1/object/attachment/{pkiAttachmentID}/getDownloadUrl
- GET /1/object/communication/{pkiCommunicationID}
- GET /1/object/ezsignfoldertype/{pkiEzsignfoldertypeID}/getDefaults
- GET /1/object/ezsigntemplate/{pkiEzsigntemplateID}
- GET /1/object/user/{pkiUserID}/getColleagues (v1)
- GET /2/object/branding/{pkiBrandingID}
- GET /2/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /2/object/ezsigntemplate/{pkiEzsigntemplateID}
- GET /2/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- GET /3/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- POST /1/object/activesession/answerSecretQuestion
- POST /1/object/branding
- POST /1/object/ezsignbulksend/{pkiEzsignbulksendID}/createEzsignbulksendtransmission
- POST /1/object/ezsigntemplate
- POST /1/object/ezsigntemplatesignature
- POST /2/object/ezsignfoldertype
- POST /2/object/ezsigntemplate
- POST /1/object/branding/{pkiBrandingID}
- PUT /1/object/ezsignfolder/{pkiEzsignfolderID}
- PUT /1/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- PUT /1/object/ezsignsignature/{pkiEzsignsignatureID}
- PUT /1/object/ezsigntemplate/{pkiEzsigntemplateID}
- PUT /1/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- PUT /1/object/user/{pkiUserID}/editColleagues
- PUT /2/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- PUT /2/object/ezsigntemplate/{pkiEzsigntemplateID}

#### Deprecated
- POST /2/object/ezsignfolder
- Property bWebhookTest in Custom-Webhook-Response

### [1.2.0] - 2024-04-14

#### Added
- DELETE /1/object/creditcardclient/{pkiCreditcardclientID}
- DELETE /1/object/discussion/{pkiDiscussionID}
- DELETE /1/object/discussionmembership/{pkiDiscussionmembershipID}
- DELETE /1/object/discussionmessage/{pkiDiscussionmessageID}
- DELETE /1/object/usergroupdelegation/{pkiUsergroupdelegationID}
- DELETE /1/object/usergroupexternal/{pkiUsergroupexternalID}
- GET /1/module/location/search
- GET /1/object/activesession/getDocumentationUrl
- GET /1/object/attachment/{pkiAttachmentID}/download
- GET /1/object/attachment/{pkiAttachmentID}/getAttachmentlogs
- GET /1/object/buyercontract/{pkiBuyercontractID}/getCommunicationList
- GET /1/object/creditcardclient/getList
- GET /1/object/discussion/{pkiDiscussionID}
- GET /1/object/electronicfundstransfer/{pkiElectronicfundstransferID}/getCommunicationList
- GET /1/object/ezsigndiscussion/{pkiEzsigndiscussionID}
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getAttachments
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsigndocumentdiscussions
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getAttachmentCount
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getAttachments
- GET /1/object/ezsignsigningreason/getAutocomplete
- GET /1/object/ezsignsigningreason/getList
- GET /1/object/ezsignsigningreason/{pkiEzsignsigningreasonID}
- GET /1/object/inscription/{pkiInscriptionID}/getAttachments
- GET /1/object/inscription/{pkiInscriptionID}/getCommunicationList
- GET /1/object/inscription/{pkiInscriptionID}/getCommunicationsenders
- GET /1/object/inscriptionnotauthenticated/{pkiInscriptionnotauthenticatedID}/getCommunicationList
- GET /1/object/inscriptiontemp/{pkiInscriptiontempID}/getCommunicationList
- GET /1/object/invoice/{pkiInvoiceID}/getAttachments
- GET /1/object/invoice/{pkiInvoiceID}/getCommunicationList
- GET /1/object/otherincome/{pkiOtherincomeID}/getCommunicationList
- GET /1/object/rejectedoffertopurchase/{pkiRejectedoffertopurchaseID}/getCommunicationList
- GET /1/object/user/{pkiUserID}/getApikeys
- GET /1/object/user/{pkiUserID}/getUsergroupexternals
- GET /1/object/user/{pkiUserID}/getUsergroups
- GET /1/object/usergroup/{pkiUsergroupID}/getUsergroupdelegations
- GET /1/object/usergroupexternal/getList
- GET /1/object/usergroupexternal/{pkiUsergroupexternalID}/getMembers
- GET /1/object/usergroupexternal/{pkiUsergroupexternalID}/getUsergroups
- GET /2/module/location/{sLocationPlaceid}
- GET /2/object/country/getAutocomplete/{sSelector}
- GET /2/object/creditcardclient/getAutocomplete/{sSelector}
- GET /2/object/creditcardclient/{pkiCreditcardclientID}
- GET /2/object/ezsigntemplateglobal/getAutocomplete/{sSelector}
- GET /2/object/ezsigntemplateglobal/{pkiEzsigntemplateglobalID}
- GET /2/object/module/getAutocomplete/{sSelector}
- GET /2/object/province/getAutocomplete/{sSelector}
- GET /2/object/usergroupdelegation/{pkiUsergroupdelegationID}
- GET /2/object/usergroupexternal/getAutocomplete/{sSelector}
- GET /2/object/usergroupexternal/{pkiUsergroupexternalID}
- PATCH /1/object/discussion/{pkiDiscussionID}
- PATCH /1/object/discussionmessage/{pkiDiscussionmessageID}
- POST /1/object/creditcardclient
- POST /1/object/discussion
- POST /1/object/discussion/{pkiDiscussionID}/updateDiscussionreadstatus
- POST /1/object/discussionmembership
- POST /1/object/discussionmessage
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/applyEzsigntemplateglobal
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/createEzsignelementsPositionedByWord
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/endPrematurely
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/reassign
- POST /1/object/ezsignsigningreason
- POST /1/object/user/{pkiUserID}/sendPasswordReset
- POST /1/object/usergroup/{pkiUsergroupID}/editUsergroupdelegations
- POST /1/object/usergroupdelegation
- POST /1/object/usergroupexternal
- POST /1/object/webhook/{pkiWebhookID}/regenerateApikey
- POST /2/object/ezsignfoldertype
- POST /2/object/webhook
- PUT /1/object/creditcardclient/{pkiCreditcardclientID}
- PUT /1/object/ezsignsigningreason/{pkiEzsignsigningreasonID}
- PUT /1/object/usergroupdelegation/{pkiUsergroupdelegationID}
- PUT /1/object/usergroupexternal/{pkiUsergroupexternalID}
- PUT /2/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- Advanced search filters sContactFirstname, sContactLastname and sEzsigndocumentName to Ezsignfolder list
- New error code 413 Content too large
- Multiple new properties across objects
- New authorization key starting with "W" for webhooks
- New iso environment for isolated customers
- Webhook Document Form Completed
- Webhook Document Unsent
- Webhook Folder Disposed
- Webhook Folder Sent
- Webhook Folder Unsent
- Webhook Signature Signed
- Support for PowerAutomate flows
- Support for Salesforce flows

#### Removed
- GET /1/object/ezmaxinvoicing/getAutocomplete/{sSelector}
- GET /1/object/ezsignfoldertype/getAutocomplete/{sSelector}
- GET /1/object/franchisebroker/getAutocomplete/{sSelector}
- GET /1/object/period/getAutocomplete/{sSelector}
- POST /1/object/activesession/answerSecretquestion
- POST /1/object/ezsignfoldersignerassociation/reassign
- POST /1/object/ezsignfoldertype
- POST /1/object/franchisereferalincome
- POST /1/object/webhook
- POST /2/object/ezsignfolder/{pkiEzsignfolderID}/send
- Support for eZmax-SDK-apex
- Support for eZmax-SDK-javascript

#### Deprecated
- POST /1/object/ezsignfoldersignerassociation/reassign
- POST /1/object/webhook
- Multiple properties related to form field groups and custom date values

---

## 1.1.X Releases

### [1.1.19] - 2023-08

#### Added
- DELETE /1/object/usergroupdelegation/{pkiUsergroupdelegationID}
- GET /1/object/activesession/getDocumentationUrl
- GET /1/object/user/{pkiUserID}/getApikeys
- GET /1/object/usergroup/{pkiUsergroupID}/getUsergroupdelegations
- GET /2/object/usergroupdelegation/{pkiUsergroupdelegationID}
- POST /1/object/user/{pkiUserID}/sendPasswordReset
- POST /1/object/usergroup/{pkiUsergroupID}/editUsergroupdelegations
- POST /1/object/usergroupdelegation
- PUT /1/object/usergroupdelegation/{pkiUsergroupdelegationID}
- Added property bVersionDeprecated in Common-Response-objDebugPayload
- Added property eEzsigndocumentSteptype in ezsigndocument-ResponseCompound
- Added property iEzsigntemplatesignatureWidth and iEzsigntemplatesignatureHeight in object ezsigntemplatesignature-Request and ezsigntemplatesignature-Response
- Added property eEzsignformfieldgroupTextvalidation in ezsignformfieldgroup-Response
- Added property eEzsigntemplateformfieldgroupTextvalidation in ezsigntemplateformfieldgroup-Request and ezsigntemplateformfieldgroup-Response
- Added property iEzsignsignatureMaxlength in ezsignsignature-Request and ezsignsignature-Response
- Added properties iEzsigntemplatesignatureMaxlength, sEzsigntemplatesignatureRegexp and eEzsigntemplatesignatureTextvalidation in ezsigntemplatesignature-Request and ezsigntemplatesignature-Response
- Added value AgentBrokerEzsignUserNormal for sSelector in GET /2/object/user/getAutocomplete/{sSelector}

### [1.1.18] - 2023-07-22

#### Added
- DELETE /1/object/cors/{pkiCorsID}
- DELETE /1/object/ezsignsignergroupmembership/{pkiEzsignsignergroupmembershipID}
- DELETE /1/object/permission/{pkiPermissionID}
- DELETE /1/object/signature/{pkiSignatureID}
- DELETE /1/object/subnet/{pkiSubnetID}
- DELETE /1/object/usergroupmembership/{pkiUsergroupmembershipID}
- DELETE /2/scim/Groups/{groupId}
- DELETE /2/scim/Users/{userId}
- GET /1/object/apikey/getList
- GET /1/object/apikey/{pkiApkiID}
- GET /1/object/apikey/{pkiApkiID}/getCors
- GET /1/object/apikey/{pkiApkiID}/getPermissions
- GET /1/object/apikey/{pkiApkiID}/getSubnets
- GET /1/module/report/getReportFromCache/{sReportgroupCacheID}
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignfoldersignerassociationsmine
- GET /1/object/ezsignsignature/{pkiEzsignsignatureID}/getEzsignsignatureattachment
- GET /1/object/modulegroup/getAll/{eContext}
- GET /1/object/user/getList
- GET /1/object/user/{pkiUserID}/getEffectivePermissions
- GET /1/object/user/{pkiUserID}/getPermissions
- GET /1/object/user/{pkiUserID}/getSubnets
- GET /1/object/usergroup/{pkiUsergroupID}/getPermissions
- GET /1/object/usergroup/{pkiUsergroupID}/getUsergroupmemberships
- GET /1/object/usergroupmembership/{pkiUsergroupmembershipID}
- GET /2/object/company/getAutocomplete/{sSelector}
- GET /2/object/cors/{pkiCorsID}
- GET /2/object/emailtype/getAutocomplete/{sSelector}
- GET /2/object/ezsignsignergroupmembership/{pkiEzsignsignergroupmembershipID}
- GET /2/object/permission/{pkiPermissionID}
- GET /2/object/phonetype/getAutocomplete/{sSelector}
- GET /2/object/signature/{pkiSignatureID}
- GET /2/object/subnet/{pkiSubnetID}
- GET /2/object/systemconfiguration/{pkiSystemconfigurationID}
- GET /2/object/user/{pkiUserID}
- GET /2/scim/Groups
- GET /2/scim/Groups/{groupId}
- GET /2/scim/ServiceProviderConfig
- GET /2/scim/Users
- GET /2/scim/Users/{userId}
- POST /1/object/apikey/{pkiApikeyID}/regenerate
- POST /1/object/cors
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/submitEzsignform
- POST /1/object/ezsignpage/{pkiEzsignpageID}/consult
- POST /1/object/ezsignsignergroupmembership
- POST /1/object/permission
- POST /1/object/signature
- POST /1/object/subnet
- POST /1/object/usergroupmembership
- POST /1/object/userstaged/{pkiUserstagedID}/createUser
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/declineToSign
- POST /1/object/user
- POST /1/report/accountsreceivable/accountsreceivablereport
- POST /2/scim/Groups
- POST /2/scim/Users
- PUT /1/object/apikey/{pkiApikeyID}
- PUT /1/object/apikey/{pkiApikeyID}/editPermissions
- PUT /1/object/cors/{pkiCorsID}
- PUT /1/object/permission/{pkiPermissionID}
- PUT /1/object/signature/{pkiSignatureID}
- PUT /1/object/subnet/{pkiSubnetID}
- PUT /1/object/systemconfiguration/{pkiSystemconfigurationID}
- PUT /1/object/user/{pkiUserID}
- PUT /1/object/user/{pkiUserID}/editPermissions
- PUT /1/object/usergroup/{pkiUsergroupID}/editPermissions
- PUT /1/object/usergroup/{pkiUsergroupID}/editUsergroupmemberships
- PUT /1/object/usergroupmembership/{pkiUsergroupmembershipID}
- PUT /2/scim/Groups/{groupId}
- PUT /2/scim/Users/{userId}
- Webhook Userstaged Created in Userstaged
- Websocket RequestServer-GetWebsocketID-V1
- Websocket Response-Error-V1
- Websocket Response-GetWebsocketID-V1
- Websocket Response-Information-V1
- Multiple new properties in various objects

#### Removed
- GET /1/object/billingentityinternal/getAutocomplete/{sSelector}
- GET /1/object/branding/{pkiBrandingID}
- GET /1/object/branding/getAutocomplete/{sSelector}
- GET /1/object/department/getAutocomplete/{sSelector}
- GET /1/object/ezmaxinvoicing/{pkiEzmaxinvoicingID}
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}
- GET /1/object/ezsignbulksenddocumentmapping/{pkiEzsignbulksenddocumentmappingID}
- GET /1/object/ezsignbulksendsignermapping/{pkiEzsignbulksendsignermappingID}
- GET /1/object/ezsignbulksendtransmission/{pkiEzsignbulksendtransmissionID}
- GET /1/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- GET /1/object/ezsignformfieldgroup/{pkiEzsignformfieldgroupID}
- GET /1/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /1/object/ezsigntemplate/getAutocomplete/{sSelector}
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}
- GET /1/object/ezsigntemplateformfieldgroup/{pkiEzsigntemplateformfieldgroupID}
- GET /1/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}
- GET /1/object/ezsigntemplatepackage/getAutocomplete/{sSelector}
- GET /1/object/ezsigntemplatepackagemembership/{pkiEzsigntemplatepackagemembershipID}
- GET /1/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- GET /1/object/ezsigntemplatepackagesignermembership/{pkiEzsigntemplatepackagesignermembershipID}
- GET /1/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- GET /1/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- GET /1/object/ezsigntsarequirement/getAutocomplete/{sSelector}
- GET /1/object/franchiseoffice/getAutocomplete/{sSelector}
- GET /1/object/secretquestion/getAutocomplete/{sSelector}
- GET /1/object/taxassignment/getAutocomplete/{sSelector}
- GET /1/object/timezone/getAutocomplete/{sSelector}
- GET /1/object/user/getAutocomplete/{sSelector}
- GET /1/object/usergroup/getAutocomplete/{sSelector}
- GET /1/object/versionhistory/{pkiVersionhistoryID}
- GET /1/object/webhook/{pkiWebhookID}
- POST /1/object/apikey

### [1.1.17] - 2023-05-22

#### Added
- DELETE /1/object/ezsignannotation/{pkiEzsignannotationID}
- DELETE /1/object/userstaged/{pkiUserstagedID}
- GET /1/ezmaxclient/{pksEzmaxclientOs}/version
- GET /1/ezmaxcustomer/{pksEzmaxcustomerCode}/getConfiguration
- GET /1/object/activesession/getList
- GET /1/object/billingentityinternal/getList
- GET /1/object/clonehistory/getList
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}/getEzsignsignaturesAutomatic
- GET /1/object/ezsignbulksendtransmission/{pkiEzsignbulksendtransmissionID}/getEzsignsignaturesAutomatic
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getCompletedElements
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignannotations
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignsignaturesAutomatic
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getCommunicationCount
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getCommunicationList
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignsignaturesAutomatic
- GET /1/object/ezsignsignature/getEzsignsignaturesAutomatic
- GET /1/object/paymentterm/getList
- GET /1/object/usergroup/getList
- GET /1/object/userstaged/getList
- GET /2/object/billingentityinternal/{pkiBillingentityinternalID}
- GET /2/object/billingentityexternal/getAutocomplete/{sSelector}
- GET /2/object/communication/{pkiCommunicationID}
- GET /2/object/ezmaxproduct/getAutocomplete/{sSelector}
- GET /2/object/ezsignannotation/{pkiEzsignannotationID}
- GET /2/object/paymentterm/{pkiPaymenttermID}
- GET /2/object/paymentterm/getAutocomplete/{sSelector}
- GET /1/object/sessionhistory/getList
- GET /2/object/usergroup/{pkiUsergroupID}
- GET /2/object/userstaged/{pkiUserstagedID}
- POST /1/object/billingentityinternal
- POST /1/object/ezsignannotation
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/flatten
- POST /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/flatten
- POST /1/object/paymentterm
- POST /1/object/usergroup
- POST /1/object/userstaged/{pkiUserstagedID}/map
- PUT /1/object/billingentityinternal/{pkiBillingentityinternalID}
- PUT /1/object/ezsignannotation/{pkiEzsignannotationID}
- PUT /1/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignannotations
- PUT /1/object/paymentterm/{pkiPaymenttermID}
- PUT /1/object/usergroup/{pkiUsergroupID}
- Webhook Ezsignsigner Accept Clause in Ezsignfoldersignerassociation
- Webhook Ezsignsigner Connect in Ezsignfoldersignerassociation
- Multiple new error codes and properties

### [1.1.16] - 2022-11-10

#### Added
- POST /1/object/ezsigntemplate/{pkiEzsigntemplateID}/copy
- Properties fkiEzsignfoldersignerassociationIDDeclinedtosign and tEzsigndocumentDeclinedtosignreason in ezsigndocument-Response

### [1.1.15] - 2022-11-07

#### Added
- PATCH /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- POST /3/object/ezsignfolder/{pkiEzsignfolderID}/send
- Enum value 'PendingSend' for eEzsignfolderStep
- Property bEzsignfoldersignerassociationDelayedsend in ezsignfoldersignerassociation-Response
- Property dtEzsignfolderDelayedsenddate in ezsignfolder-Response

#### Deprecated
- POST /2/object/ezsignfolder/{pkiEzsignfolderID}/send

### [1.1.14] - 2022-11-01

#### Added
- GET /2/object/period/getAutocomplete/{sSelector}
- GET /2/object/franchisebroker/getAutocomplete/{sSelector}
- GET /2/object/franchiseoffice/getAutocomplete/{sSelector}

#### Deprecated
- GET /1/object/period/getAutocomplete/{sSelector}
- GET /1/object/franchisebroker/getAutocomplete/{sSelector}
- GET /1/object/franchiseoffice/getAutocomplete/{sSelector}

### [1.1.13] - 2022-10-28

#### Added
- GET /1/object/ezmaxinvoicing/getAutocomplete/{sSelector}
- GET /1/object/ezmaxinvoicing/getProvisional
- GET /1/object/ezmaxinvoicing/{pkiEzmaxinvoicingID}
- GET /2/object/billingentityinternal/getAutocomplete/{sSelector}
- GET /2/object/branding/getAutocomplete/{sSelector}
- GET /2/object/department/getAutocomplete/{sSelector}
- GET /2/object/ezmaxinvoicing/getAutocomplete/{sSelector}
- GET /2/object/ezsignfoldertype/getAutocomplete/{sSelector}
- GET /2/object/ezsigntemplate/getAutocomplete/{sSelector}
- GET /2/object/ezsigntemplatepackage/getAutocomplete/{sSelector}
- GET /2/object/ezsigntsarequirement/getAutocomplete/{sSelector}
- GET /2/object/secretquestion/getAutocomplete/{sSelector}
- GET /2/object/taxassignment/getAutocomplete/{sSelector}
- GET /2/object/timezone/getAutocomplete/{sSelector}
- GET /2/object/user/getAutocomplete/{sSelector}
- GET /2/object/usergroup/getAutocomplete/{sSelector}
- GET /2/object/branding/{pkiBrandingID}
- GET /2/object/ezmaxinvoicing/{pkiEzmaxinvoicingID}
- GET /2/object/ezsignbulksend/{pkiEzsignbulksendID}
- GET /2/object/ezsignbulksenddocumentmapping/{pkiEzsignbulksenddocumentmappingID}
- GET /2/object/ezsignbulksendsignermapping/{pkiEzsignbulksendsignermappingID}
- GET /2/object/ezsignbulksendtransmission/{pkiEzsignbulksendtransmissionID}
- GET /2/object/ezsigndocument/{pkiEzsigndocumentID}
- GET /2/object/ezsignfolder/{pkiEzsignfolderID}
- GET /2/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- GET /2/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- GET /2/object/ezsignformfieldgroup/{pkiEzsignformfieldgroupID}
- GET /2/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /2/object/ezsigntemplate/{pkiEzsigntemplateID}
- GET /2/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}
- GET /2/object/ezsigntemplateformfieldgroup/{pkiEzsigntemplateformfieldgroupID}
- GET /2/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}
- GET /2/object/ezsigntemplatepackagemembership/{pkiEzsigntemplatepackagemembershipID}
- GET /2/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- GET /2/object/ezsigntemplatepackagesignermembership/{pkiEzsigntemplatepackagesignermembershipID}
- GET /2/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- GET /2/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- GET /2/object/webhook/{pkiWebhookID}
- Accepted value 'Attachments' for field eEzsigntemplatesignatureType
- Multiple new properties and error codes

#### Deprecated
- GET /1/object/billingentityinternal/getAutocomplete/{sSelector}
- GET /1/object/branding/getAutocomplete/{sSelector}
- GET /1/object/department/getAutocomplete/{sSelector}
- GET /1/object/ezmaxinvoicing/getAutocomplete/{sSelector}
- GET /1/object/ezsignfoldertype/getAutocomplete/{sSelector}
- GET /1/object/ezsigntemplate/getAutocomplete/{sSelector}
- GET /1/object/ezsigntemplatepackage/getAutocomplete/{sSelector}
- GET /1/object/ezsigntsarequirement/getAutocomplete/{sSelector}
- GET /1/object/secretquestion/getAutocomplete/{sSelector}
- GET /1/object/taxassignment/getAutocomplete/{sSelector}
- GET /1/object/timezone/getAutocomplete/{sSelector}
- GET /1/object/user/getAutocomplete/{sSelector}
- GET /1/object/usergroup/getAutocomplete/{sSelector}
- GET /1/object/branding/{pkiBrandingID}
- GET /1/object/ezmaxinvoicing/{pkiEzmaxinvoicingID}
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}
- GET /1/object/ezsignbulksenddocumentmapping/{pkiEzsignbulksenddocumentmappingID}
- GET /1/object/ezsignbulksendsignermapping/{pkiEzsignbulksendsignermappingID}
- GET /1/object/ezsignbulksendtransmission/{pkiEzsignbulksendtransmissionID}
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}
- GET /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- GET /1/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- GET /1/object/ezsignformfieldgroup/{pkiEzsignformfieldgroupID}
- GET /1/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /1/object/ezsigntemplate/{pkiEzsigntemplateID}
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}
- GET /1/object/ezsigntemplateformfieldgroup/{pkiEzsigntemplateformfieldgroupID}
- GET /1/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}
- GET /1/object/ezsigntemplatepackagemembership/{pkiEzsigntemplatepackagemembershipID}
- GET /1/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- GET /1/object/ezsigntemplatepackagesignermembership/{pkiEzsigntemplatepackagesignermembershipID}
- GET /1/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- GET /1/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- GET /1/object/webhook/{pkiWebhookID}

#### Fixed
- (CSharpSDK) We now use the correct encoding of the fingerprint for signing requests
- (CSharpSDK) We can now use variable properties object i.e: /1/object/notificationtest/{pkiNotificationtestID}/getElements

### [1.1.12] - Skipped

### [1.1.11] - Skipped

### [1.1.10] - 2022-08-23

#### Added
- DELETE /1/object/webhook/{pkiWebhookID}
- GET /1/object/branding/{pkiBrandingID}
- GET /1/object/branding/getList
- GET /1/object/department/getAutocomplete/{sSelector}
- GET /1/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- GET /1/object/webhook/{pkiWebhookID}
- GET /1/object/webhook/{pkiWebhookID}/getHistory
- GET /1/object/webhook/getList
- POST /1/object/branding
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/importEzsignfoldersignerassociations
- POST /1/object/ezsignfoldertype
- POST /1/object/webhook
- POST /1/object/webhook/{pkiWebhookID}/test
- POST /2/object/ezsignfolder/{pkiEzsignfolderID}/send
- PUT /1/object/branding/{pkiBrandingID}
- PUT /1/object/ezsignfoldertype/{pkiEzsignfoldertypeID}
- PUT /1/object/webhook/{pkiWebhookID}
- New supported eEzsignsignatureType: Attachments
- Object Custom-EzsignfoldersignerassociationActionableElement-Response
- Multiple new properties in ezsignsignature and ezsignfoldertype objects

#### Changed
- The return object for route GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignfoldersignerassociations is now of type Custom-EzsignfoldersignerassociationActionableElement-Response

#### Deprecated
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/send

### [1.1.9] - 2022-06-20

#### Changed
- Property dtEzsigndocumentFirstsend in Ezsigndocument is no longer required
- Property dtEzsigndocumentLastsend in Ezsigndocument is no longer required
- Property dtEzsignfolderClose in Ezsignfolder is no longer required

### [1.1.8] - 2022-06-20

#### Added
- GET /1/object/activesession/getCurrent fkiTimezoneID, eUserEzsignsendreminderfrequency, iUserInterfacecolor, bUserInterfacedark and iUserListresult
- GET /1/object/billingentityinternal/getAutocomplete/{sSelector}
- GET /1/object/branding/getAutocomplete/{sSelector}
- GET /1/object/notificationtest/{pkiNotificationtestID}/getElements
- GET /1/object/taxassignment/getAutocomplete/{sSelector}
- GET /1/object/timezone/getAutocomplete/{sSelector}
- GET /1/object/user/getAutocomplete/{sSelector}
- GET /1/object/usergroup/getAutocomplete/{sSelector}
- Warning Code MUSTVERIFY added to documentation

#### Changed
- Property dtEzsignfolderScheduledarchive in Ezsignfolder is no longer required
- Property dtEzsignfolderScheduleddispose in Ezsignfolder is no longer required

### [1.1.7] - 2022-05-17

#### Added
- DELETE /1/object/ezsignbulksend/{pkiEzsignbulksendID}
- DELETE /1/object/ezsignbulksenddocumentmapping/{pkiEzsignbulksenddocumentmappingID}
- DELETE /1/object/ezsignbulksendsignermapping/{pkiEzsignbulksendsignermappingID}
- DELETE /1/object/ezsigntemplate/{pkiEzsigntemplateID}
- DELETE /1/object/ezsigntemplateformfieldgroup/{pkiEzsigntemplateformfieldgroupID}
- DELETE /1/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}
- DELETE /1/object/ezsigntemplatepackagemembership/{pkiEzsigntemplatepackagemembershipID}
- DELETE /1/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- DELETE /1/object/ezsigntemplatepackagesignermembership/{pkiEzsigntemplatepackagesignermembershipID}
- DELETE /1/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- DELETE /1/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- GET /1/module/ezsign/suggestSigners
- GET /1/module/ezsign/suggestTemplates
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}/getCsvTemplate
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}/getFormsData
- GET /1/object/ezsignbulksenddocumentmapping/{pkiEzsignbulksenddocumentmappingID}
- GET /1/object/ezsignbulksendsignermapping/{pkiEzsignbulksendsignermappingID}
- GET /1/object/ezsignbulksendtransmission/{pkiEzsignbulksendtransmissionID}/getCsvErrors
- GET /1/object/ezsignbulksendtransmission/{pkiEzsignbulksendtransmissionID}/getFormsData
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignsignatures properties
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getActionableElements
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/batchDownload
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getActionableElements
- GET /1/object/ezsignfoldertype/getAutocomplete/{sSelector}
- GET /1/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /1/object/ezsigntemplate/{pkiEzsigntemplateID}
- GET /1/object/ezsigntemplate/getAutocomplete/{sSelector}
- GET /1/object/ezsigntemplate/getList
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplateformfieldgroups
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplatedocumentpages
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getEzsigntemplatesignatures
- GET /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/getWordsPositions
- GET /1/object/ezsigntemplateformfieldgroup/{pkiEzsigntemplateformfieldgroupID}
- GET /1/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}
- GET /1/object/ezsigntemplatepackage/getAutocomplete/{sSelector}
- GET /1/object/ezsigntemplatepackagemembership/{pkiEzsigntemplatepackagemembershipID}
- GET /1/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- GET /1/object/ezsigntemplatepackagesignermembership/{pkiEzsigntemplatepackagesignermembershipID}
- GET /1/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- GET /1/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- GET /1/object/ezsigntsarequirement/getAutocomplete/{sSelector}
- GET /1/object/notificationsection/{pkiNotificationsectionID}/getNotificationtests
- GET /1/object/secretquestion/getAutocomplete/{sSelector}
- PATCH /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}
- POST /1/object/ezsignbulksend
- POST /1/object/ezsignbulksend/{pkiEzsignbulksendID}/createEzsignbulksendtransmission
- POST /1/object/ezsignbulksend/{pkiEzsignbulksendID}/reorder
- POST /1/object/ezsignbulksenddocumentmapping
- POST /1/object/ezsignbulksendsignermapping
- POST /2/object/ezsigndocument properties
- POST /1/object/ezsigndocument properties
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/unsend
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/archive
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/importEzsigntemplatepackage
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/reorder
- POST /1/object/ezsignsignature properties
- POST /2/object/ezsignsignature properties
- POST /1/object/ezsignsignature/{pkiEzsignsignatureID}/sign
- POST /1/object/ezsigntemplate
- POST /1/object/ezsigntemplatedocument
- POST /1/object/ezsigntemplateformfieldgroup
- POST /1/object/ezsigntemplatepackage
- POST /1/object/ezsigntemplatepackagemembership
- POST /1/object/ezsigntemplatepackagesigner
- POST /1/object/ezsigntemplatepackagesignermembership
- POST /1/object/ezsigntemplatesignature
- POST /1/object/ezsigntemplatesigner
- PUT /1/object/ezsignbulksend/{pkiEzsignbulksendID}
- PUT /1/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignsignatures
- PUT /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- PUT /1/object/ezsignsignature/{pkiEzsignsignatureID}
- PUT /1/object/ezsigntemplate
- PUT /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}
- PUT /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/editEzsigntemplateformfieldgroups
- PUT /1/object/ezsigntemplatedocument/{pkiEzsigntemplatedocumentID}/editEzsigntemplatesignatures
- PUT /1/object/ezsigntemplateformfieldgroup/{pkiEzsigntemplateformfieldgroupID}
- PUT /1/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}
- PUT /1/object/ezsigntemplatepackage/{pkiEzsigntemplatepackageID}/editEzsigntemplatepackagesigners
- PUT /1/object/ezsigntemplatepackagesigner/{pkiEzsigntemplatepackagesignerID}
- PUT /1/object/ezsigntemplatesignature/{pkiEzsigntemplatesignatureID}
- PUT /1/object/ezsigntemplatesigner/{pkiEzsigntemplatesignerID}
- Error codes documentation

#### Deprecated
- /1/object/ezsignfoldertype/getAutocomplete/{sSelector} mValue

### [1.1.6] - 2022-03-04

#### Added
- DELETE /1/object/ezsignformfieldgroup/{pkiEzsignformfieldgroupID}
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}/getEzsignbulksendtransmissions
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignformfieldgroups
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignsignatures
- GET /1/object/ezsignformfieldgroup/{pkiEzsignformfieldgroupID}
- GET /1/object/ezsignsignature/{pkiEzsignsignatureID}
- POST /1/object/ezsignformfieldgroup
- POST /2/object/apikey
- POST /2/object/ezsigndocument
- POST /2/object/ezsignfolder
- POST /2/object/ezsignfoldersignerassociation
- POST /2/object/ezsignsignature
- POST /2/object/franchisereferalincome
- PUT /1/object/ezsignformfieldgroup/{pkiEzsignformfieldgroupID}
- PUT /1/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignformfieldgroups

#### Changed
- Audit in return response has been hierarchized

#### Deprecated
- POST /1/object/apikey
- POST /1/object/ezsigndocument
- POST /1/object/ezsignfolder
- POST /1/object/ezsignfoldersignerassociation
- POST /1/object/ezsignsignature
- POST /1/object/franchisereferalincome

### [1.1.4] - 2022-02-24

#### Added
- GET /1/object/ezsignbulksend/{pkiEzsignbulksendID}
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID} Added status
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getTemporaryProof
- GET /1/object/ezsignfolder/{pkiEzsignfolderID} Added multiple properties
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsigndocuments
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getEzsignfoldersignerassociations
- GET /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- PATCH /1/object/ezsigndocument/{pkiEzsigndocumentID}
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/endPrematurely
- POST /1/object/ezsignsignature properties
- PUT /1/object/ezsigndocument/{pkiEzsigndocumentID}/editEzsignsignatures
- PUT /1/object/ezsignfolder/{pkiEzsignfolderID}
- Multiple new error codes

### [1.1.3] - 2021-12-17

#### Added
- GET /1/object/ezsignbulksend/getList
- GET /1/object/ezsigntemplatepackage/getList
- POST /1/object/ezsignfoldersignerassociation bEzsignfoldersignerassociationReceivecopy property
- Multiple new error codes

#### Changed
- Changed all the OneOf used back to nullable types

#### Fixed
- (AxiosSDK) Fingerprint header on GET requests was invalid when url parameters contained utf8 special chars
- (CsharpSDK) OneOf not supported for polymorphism was preventing compilation

### [1.1.2] - 2021-10-26

#### Added
- GET /1/object/ezsignfolder/getList eEzsignfoldertypePrivacylevel property
- POST /1/object/ezsigndocument returns a sTemporaryFileUrl on error 422 if error is recoverable
- POST /1/object/ezsigndocument sEzsigndocumentUrl property
- POST /1/object/ezsigndocument eEzsigndocumentSource property now accept "Url" as the source
- POST /1/object/ezsigndocument bEzsigndocumentForcerepair property
- Support for "rg" operator in date fields in sFilter
- Range operator added to convention section of the documentation

### [1.1.1] - 2021-10-22

#### Added
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/unsend
- GET /1/module/list/listpresentation/{sListName}
- POST /1/module/list/listpresentation/{sListName}
- Variables convention documentation
- POST /1/object/ezsigndocument/ sEzsigndocumentPassword property
- Support for "in" operator for integer fields in sFilter
- Support for "in" operator for enum fields in sFilter

### [1.1.0] - 2021-10-19

#### Added
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getEzsignpages
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getFormData
- GET /1/object/ezsignfolder/{pkiEzsignfolderID}/getFormsData
- GET /1/object/ezsignfolder/getList
- GET /1/object/ezsignfoldertype/getAutocomplete/{sSelector}
- GET /1/object/ezsignfoldertype/getList
- POST /2/object/ezsigndocument/{pkiEzsigndocumentID}/applyEzsigntemplate
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/getWordsPositions
- Multiple new status codes and error codes
- Variables convention added to documentation
- List Filter convention added to documentation

#### Deprecated
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/applyezsigntemplate

#### Removed
- Support for typescript-angular
- Support for typescript-aurelia
- Support for typescript-fetch
- Support for typescript-jquery
- Support for typescript-node

#### Fixed
- (AxiosSDK) Fingerprint header on GET requests was invalid when url parameters were used

---

## 1.0.X Releases

### [1.0.47] - 2021-09-20

#### Early Adopters
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/getWordsPositions
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getFormsData

#### Added
- Early Adopters mention in documentation for endpoints not ready to be used in production

#### Changed
- Normalized internal definition of AllOf (Objects vs additionnal properties)

#### Fixed
- (CsharpSDK) Requests don't have to be mandatory signed anymore

### [1.0.46] - 2021-06-03

#### Fixed
- Minor changes

### [1.0.45] - 2021-06-02

#### Added
- Enum values "DeclinedToSign" and "PrematurelyEnded" to field eEzsigndocumentStep

### [1.0.44] - 2021-05-31

#### Added
- Enum value "City" for Ezsignsignature
- Password can be sent in encrypted form in authenticate method

#### Fixed
- (AxiosSDK) Fingerprint header on GET requests was sometimes invalid

### [1.0.43] - 2021-05-25

#### Added
- (SDK) cpp-qt-client
- POST /2/module/authenticate/authenticate/{eSessionType}

#### Removed
- (SDK) cpp-qt5-client

### [1.0.42] - 2021-04-21

#### Changed
- (AxiosSDK) Minor changes

### [1.0.41] - 2021-04-21

#### Changed
- (AxiosSDK) Minor changes

### [1.0.40] - 2021-04-19

#### Changed
- (AxiosSDK) Minor changes

### [1.0.39] - 2021-03-26

#### Added
- (CsharpSDK) Automatic request signing
- (CsharpSDK) Secret handling in configuration class
- eErrorCode in Error model
- Error Codes documentation section
- Documentation for 350 Redirection code (Authentication)

#### Changed
- Signature algorithm now supports HMAC SHA256

### [1.0.38] - 2021-03-22

#### Fixed
- (CsharpSDK) Hyphens in Class Name

### [1.0.37] - 2021-03-18

#### Added
- (AxiosSDK) Published to NPM

#### Changed
- (AxiosSDK) Minor changes

### [1.0.33] - 2021-03-14

#### Added
- (PHPSDK) Automatic request signing
- (PHPSDK) Secret handling in configuration class
- (AxiosSDK) Automatic request signing
- (AxiosSDK) Secret handling in configuration class

#### Fixed
- Extra slash in /1/module/sspr/resetPasswordRequest

### [1.0.32] - 2021-03-05

#### Added
- POST /1/module/sspr/validateToken
- Webhooks successful codes in Status Codes documentation section
- fkiUserID in the response of Activesession getCurrent
- fkiApikeyID in the response of Activesession getCurrent

#### Changed
- Webhooks now consider an HTTP Code of 202 to be a successful delivery
- Minor changes

#### Removed
- sEzsigndocumentFilename in the request of Create Ezsigndocument
- sEzsigndocumentFilename in the response of Create Ezsigndocument

### [1.0.31] - 2021-02-28

#### Added
- Changelog section in documentation
- Special type Authorization key
- Security section in documentation
- Request Signing section in documentation
- POST /1/module/sspr/unlockAccountRequest
- POST /1/module/sspr/unlockAccount
- POST /1/module/sspr/resetPasswordRequest
- POST /1/module/sspr/resetPassword
- POST /1/module/sspr/validateToken

#### Changed
- Authorization section moved under security section in documentation

#### Removed
- PUT /1/object/ezsigndocument/{pkiEzsigndocumentID}
- PUT /1/object/ezsignfolder/{pkiEzsignfolderID}
- PUT /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- PUT /1/object/ezsignsignature/{pkiEzsignsignatureID}

### [1.0.30] - 2021-02-12

#### Added
- Added global endpoint in servers list
- POST /1/module/sspr/sendUsernames
- Introduction section in documentation
- Servers section in documentation
- Authorization section in documentation
- Status Codes section in documentation
- Webhooks section in documentation

### [1.0.29] - 2021-02-10

#### Added
- GET /1/customer/{pksCustomerCode}/endpoint

### [1.0.28] - 2021-02-04

#### Changed
- Minor changes

### [1.0.27] - 2021-02-03

#### Changed
- Minor changes

### [1.0.26] - 2021-01-08

#### Added
- Added Audit objets to some responses

### [1.0.25] - 2021-01-08

#### Changed
- Minor changes

### [1.0.24] - 2021-01-07

#### Added
- POST /1/object/apikey

### [1.0.23] - 2020-12-21

#### Changed
- Minor changes

### [1.0.22] - 2020-12-21

#### Changed
- Minor changes

### [1.0.21] - 2020-12-21

#### Added
- WEBHOOK User-UserCreated

### [1.0.20] - 2020-12-17

#### Added
- POST /1/module/user/createezsignuser
- POST /1/object/ezsigndocument/{pkiEzsigndocumentID}/applyezsigntemplate

#### Changed
- Reorganized Documentation Categories

### [1.0.19] - 2020-12-01

#### Changed
- Minor changes

### [1.0.18] - 2020-10-14

#### Changed
- Minor changes

### [1.0.17] - 2020-09-30

#### Changed
- Minor changes

### [1.0.16] - 2020-09-29

#### Added
- GET /1/object/franchisebroker/getAutocomplete/{sSelector}

### [1.0.15] - 2020-09-28

#### Removed
- GET /1/object/period/getAutocomplete

#### Added
- GET /1/object/period/getAutocomplete/{sSelector}

### [1.0.14] - 2020-09-28

#### Added
- GET /1/object/period/getAutocomplete

### [1.0.13] - 2020-09-08

#### Changed
- Minor changes

### [1.0.12] - 2020-09-08

#### Changed
- Minor changes

### [1.0.11] - 2020-09-04

#### Added
- POST /1/object/franchisereferalincome/

### [1.0.10] - 2020-08-11

#### Changed
- Minor changes

### [1.0.9] - 2020-08-06

#### Added
- GET /1/object/ezsigndocument/{pkiEzsigndocumentID}/getDownloadUrl/{eDocumentType}
- GET /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}/getInPersonLoginUrl

### [1.0.8] - 2020-08-04

#### Changed
- Minor changes

### [1.0.7] - 2020-07-29

#### Changed
- Minor changes

### [1.0.6] - 2020-07-29

#### Changed
- Minor changes

### [1.0.5] - 2020-07-29

#### Added
- WEBHOOK Ezsign-DocumentCompleted
- WEBHOOK Ezsign-FolderCompleted

### [1.0.4] - 2020-07-09

#### Added
- POST /1/object/ezsignsignature
- GET /1/object/ezsignsignature/{pkiEzsignsignatureID}
- DELETE /1/object/ezsignsignature/{pkiEzsignsignatureID}
- GET /1/object/ezsignsignature/{pkiEzsignsignatureID}/getChildren

### [1.0.3] - 2020-07-08

#### Changed
- Documentation improvement

### [1.0.2] - 2020-07-26

#### Added
- GET /1/object/activesession/getCurrent
- POST /1/object/ezsignfoldersignerassociation
- GET /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- DELETE /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}
- GET /1/object/ezsignfoldersignerassociation/{pkiEzsignfoldersignerassociationID}/getChildren
- POST /1/object/ezsignfolder/{pkiEzsignfolderID}/send

### [1.0.1] - 2020-06-26

#### Changed
- Minor changes

### [1.0.0] - 2020-06-26

#### Added
- Initial Release
