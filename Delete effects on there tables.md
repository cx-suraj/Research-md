## Brands
``` sql
Executing (default): SELECT `id`, `uuid`, `userId`, `brandId`, `uname`, `name`, `profile_image`, `description`, `objective`, `guidelines`, `tac`, `budget`, `roi`, `product_url`, `category`, `start_date`, `end_date`, `stage`, `approval`, `approval_reason`, `approval_date`, `accepted_status`, `accepted_date`, `suggested_collaborators`, `purposed_collaborators`, `has_report`, `is_uploaded`, `status`, `metadata`, `created_at`, `updated_at` FROM `campaigns` AS `Campaign` WHERE `Campaign`.`brandId` = 1;

Executing (default): SELECT `id`, `campaignId`, `uuid`, `header`, `statistics`, `collaborators`, `collaborator_statistics`, `public`, `published`, `published_at`, `published_url`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_reports` AS `CampaignReport` WHERE `CampaignReport`.`campaignId` = 1;

Executing (default): SELECT `id`, `userId`, `creatorId`, `campaignId`, `uuid`, `uname`, `script`, `script_feedback`, `creator_script_status`, `admin_script_status`, `brand_script_status`, `deliverable`, `deliverable_feedback`, `creator_deliverable_status`, `admin_deliverable_status`, `brand_deliverable_status`, `deliverable_link`, `deliverable_link_feedback`, `creator_deliverable_link_status`, `admin_deliverable_link_status`, `brand_deliverable_link_status`, `stage`, `social_media`, `tac_signed`, `insight`, `creator_insight_status`, `dogl`, `creator_charge`, `creator_payment`, `creator_payment_status`, `creator_deliverables`, `apply_status`, `apply_date`, `onboard_status`, `onboard_date`, `shortlist_status`, `shortlist_date`, `contact_info`, `creator_invoice_status`, `creator_invoice_feedback`, `completed`, `status`, `created_at`, `updated_at` FROM `collaborations` AS `Collaboration` WHERE `Collaboration`.`campaignId` = 1;

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`campaignId` = 1;

Executing (default): DELETE FROM `campaigns` WHERE `id` = 1

Executing (default): SELECT `uuid`, `brandId`, `categoryId`, `updated_at`, `created_at` FROM `brand_categories` AS `BrandCategory` WHERE `BrandCategory`.`brandId` = 1;

Executing (default): DELETE FROM `brand_categories` WHERE `brandId` = 1 AND `categoryId` = 1

Executing (default): DELETE FROM `brand_categories` WHERE `brandId` = 1 AND `categoryId` = 2

Executing (default): DELETE FROM `brand_categories` WHERE `brandId` = 1 AND `categoryId` = 3

Executing (default): DELETE FROM `brand_categories` WHERE `brandId` = 1 AND `categoryId` = 6

Executing (default): SELECT `id`, `uuid`, `uname`, `brandId`, `name`, `description`, `profile_image`, `cover_image`, `stage`, `published`, `published_at`, `published_url`, `campaign_details`, `created_by`, `status`, `metadata`, `created_at`, `updated_at` FROM `proposals` AS `Proposal` WHERE `Proposal`.`brandId` = 1;

Executing (default): SELECT `uuid`, `brandId`, `regionId`, `created_at`, `updated_at` FROM `brand_regions` AS `BrandRegion` WHERE `BrandRegion`.`brandId` = 1;

Executing (default): DELETE FROM `brand_regions` WHERE `brandId` = 1 AND `regionId` = 417

Executing (default): DELETE FROM `brands` WHERE `id` = 1

*/
```

## Campaigns
```sql
Executing (default): SELECT `id`, `campaignId`, `uuid`, `header`, `statistics`, `collaborators`, `collaborator_statistics`, `public`, `published`, `published_at`, `published_url`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_reports` AS `CampaignReport` WHERE `CampaignReport`.`campaignId` = 2;

Executing (default): SELECT `id`, `userId`, `creatorId`, `campaignId`, `uuid`, `uname`, `script`, `script_feedback`, `creator_script_status`, `admin_script_status`, `brand_script_status`, `deliverable`, `deliverable_feedback`, `creator_deliverable_status`, `admin_deliverable_status`, `brand_deliverable_status`, `deliverable_link`, `deliverable_link_feedback`, `creator_deliverable_link_status`, `admin_deliverable_link_status`, `brand_deliverable_link_status`, `stage`, `social_media`, `tac_signed`, `insight`, `creator_insight_status`, `dogl`, `creator_charge`, `creator_payment`, `creator_payment_status`, `creator_deliverables`, `apply_status`, `apply_date`, `onboard_status`, `onboard_date`, `shortlist_status`, `shortlist_date`, `contact_info`, `creator_invoice_status`, `creator_invoice_feedback`, `completed`, `status`, `created_at`, `updated_at` FROM `collaborations` AS `Collaboration` WHERE `Collaboration`.`campaignId` = 2;

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 1;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 1

Executing (default): DELETE FROM `collaborations` WHERE `id` = 1

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 2;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 2

Executing (default): DELETE FROM `collaborations` WHERE `id` = 2

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 3;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 3

Executing (default): DELETE FROM `collaborations` WHERE `id` = 3

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 4;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 4

Executing (default): DELETE FROM `collaborations` WHERE `id` = 4

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 5;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 5

Executing (default): DELETE FROM `collaborations` WHERE `id` = 5

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 6;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 6

Executing (default): DELETE FROM `collaborations` WHERE `id` = 6

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 7;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 7

Executing (default): DELETE FROM `collaborations` WHERE `id` = 7

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 8;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 8

Executing (default): DELETE FROM `collaborations` WHERE `id` = 8

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 9;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 9

Executing (default): DELETE FROM `collaborations` WHERE `id` = 9

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 10;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 10

Executing (default): DELETE FROM `collaborations` WHERE `id` = 10

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`campaignId` = 2;

Executing (default): DELETE FROM `campaigns` WHERE `id` = 2

*/
```
## Tags
```sql
Executing (default): SELECT `uuid`, `creatorId`, `tagId`, `created_at`, `updated_at` FROM `creator_tags` AS `CreatorTags` WHERE `CreatorTags`.`tagId` = 1;

Executing (default): DELETE FROM `creator_tags` WHERE `creatorId` = 59 AND `tagId` = 1

Executing (default): DELETE FROM `creator_tags` WHERE `creatorId` = 107 AND `tagId` = 1

Executing (default): DELETE FROM `creator_tags` WHERE `creatorId` = 112 AND `tagId` = 1

Executing (default): DELETE FROM `creator_tags` WHERE `creatorId` = 113 AND `tagId` = 1

Executing (default): DELETE FROM `tags` WHERE `id` = 1
```
## Regions
``` sql
Executing (default): SELECT `uuid`, `creatorId`, `regionId`, `created_at`, `updated_at` FROM `creator_regions` AS `CreatorRegion` WHERE `CreatorRegion`.`regionId` = 1;

Executin
g (default): SELECT `uuid`, `brandId`, `regionId`, `created_at`, `updated_at` FROM `brand_regions` AS `BrandRegion` WHERE `BrandRegion`.`regionId` = 1;

Executing (default): DELETE FROM `regions` WHERE `id` = 1
```
## Proposal
``` sql
Executing (default): SELECT `id`, `uuid`, `uname`, `proposalId`, `creatorId`, `intent`, `intent_reason`, `intent_submitted`, `intent_submitted_at`, `platform`, `deliverables`, `commercial_price`, `relevance`, `relevance_reason`, `relevance_submitted`, `relevance_submitted_at`, `form_image`, `form_template`, `form_data`, `form_status`, `sharing_options`, `metadata`, `status`, `created_at`, `updated_at`, `ProposalId` FROM `creator_proposals` AS `CreatorProposal` WHERE `CreatorProposal`.`ProposalId` = 1;

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 1

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 2

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 3

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 4

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 5

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 6

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 7

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 8

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 9

Executing (default): DELETE FROM `creator_proposals` WHERE `id` = 10

Executing (default): DELETE FROM `proposals` WHERE `id` = 1
```
## Creator List
``` sql
Executing (default): DELETE FROM `creator_lists` WHERE `id` = 1
```

## Creators
``` sql
Executing (default): SELECT `id`, `userId`, `creatorId`, `campaignId`, `uuid`, `uname`, `script`, `script_feedback`, `creator_script_status`, `admin_script_status`, `brand_script_status`, `deliverable`, `deliverable_feedback`, `creator_deliverable_status`, `admin_deliverable_status`, `brand_deliverable_status`, `deliverable_link`, `deliverable_link_feedback`, `creator_deliverable_link_status`, `admin_deliverable_link_status`, `brand_deliverable_link_status`, `stage`, `social_media`, `tac_signed`, `insight`, `creator_insight_status`, `dogl`, `creator_charge`, `creator_payment`, `creator_payment_status`, `creator_deliverables`, `apply_status`, `apply_date`, `onboard_status`, `onboard_date`, `shortlist_status`, `shortlist_date`, `contact_info`, `creator_invoice_status`, `creator_invoice_feedback`, `completed`, `status`, `created_at`, `updated_at` FROM `collaborations` AS `Collaboration` WHERE `Collaboration`.`creatorId` = 100;

Executing (default): SELECT `uuid`, `creatorId`, `categoryId`, `created_at`, `updated_at` FROM `creator_categories` AS `CreatorCategory` WHERE `CreatorCategory`.`creatorId` = 100;

Executing (default): DELETE FROM `creator_categories` WHERE `creatorId` = 100 AND `categoryId` = 42

Executing (default): SELECT `uuid`, `creatorId`, `regionId`, `created_at`, `updated_at` FROM `creator_regions` AS `CreatorRegion` WHERE `CreatorRegion`.`creatorId` = 100;

Executing (default): DELETE FROM `creator_regions` WHERE `creatorId` = 100 AND `regionId` = 658

Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`creatorId` = 100;

Executing (default): SELECT `id`, `uuid`, `uname`, `proposalId`, `creatorId`, `intent`, `intent_reason`, `intent_submitted`, `intent_submitted_at`, `platform`, `deliverables`, `commercial_price`, `relevance`, `relevance_reason`, `relevance_submitted`, `relevance_submitted_at`, `form_image`, `form_template`, `form_data`, `form_status`, `sharing_options`, `metadata`, `status`, `created_at`, `updated_at`, `ProposalId` FROM `creator_proposals` AS `CreatorProposal` WHERE `CreatorProposal`.`creatorId` = 100;

Executing (default): SELECT `uuid`, `creatorId`, `tagId`, `created_at`, `updated_at` FROM `creator_tags` AS `CreatorTags` WHERE `CreatorTags`.`creatorId` = 100;

Executing (default): DELETE FROM `creator_tags` WHERE `creatorId` = 100 AND `tagId` = 60

Executing (default): DELETE FROM `creator_tags` WHERE `creatorId` = 100 AND `tagId` = 120

Executing (default): DELETE FROM `creator_tags` WHERE `creatorId` = 100 AND `tagId` = 121

Executing (default): SELECT `uuid`, `creatorId`, `languageId`, `created_at`, `updated_at` FROM `creator_languages` AS `CreatorLanguages` WHERE `CreatorLanguages`.`creatorId` = 100;

Executing (default): DELETE FROM `creator_languages` WHERE `creatorId` = 100 AND `languageId` = 2

Executing (default): DELETE FROM `creator_languages` WHERE `creatorId` = 100 AND `languageId` = 3

Executing (default): DELETE FROM `creator_languages` WHERE `creatorId` = 100 AND `languageId` = 4

Executing (default): DELETE FROM `creator_languages` WHERE `creatorId` = 100 AND `languageId` = 5

Executing (default): DELETE FROM `creator_languages` WHERE `creatorId` = 100 AND `languageId` = 6

Executing (default): DELETE FROM `creator_languages` WHERE `creatorId` = 100 AND `languageId` = 7

Executing (default): DELETE FROM `creators` WHERE `id` = 100
```
## Collaborations
``` sql
Executing (default): SELECT `id`, `creatorId`, `campaignId`, `collaborationId`, `uuid`, `invoice_number`, `invoice_date`, `invoice_link`, `creator_details`, `has_gst`, `creator_gst`, `has_tds`, `creator_tds`, `company_details`, `deliverables`, `creator_signature`, `total_payment_amount`, `advance_payment_amount`, `advance_payment_remaks`, `advance_payment_status`, `advance_payment_date`, `due_payment_amount`, `due_payment_remaks`, `due_payment_status`, `due_payment_date`, `creator_invoice_remaks`, `payment_proof`, `invoice_status`, `total_amount`, `subtotal_amount`, `invoice_feedback`, `is_uploaded`, `metadata`, `status`, `created_at`, `updated_at` FROM `campaign_invoices` AS `CampaignInvoice` WHERE `CampaignInvoice`.`collaborationId` = 11;

Executing (default): DELETE FROM `campaign_invoices` WHERE `id` = 11

Executing (default): DELETE FROM `collaborations` WHERE `id` = 11
```
## Categories
```sql
Executing (default): SELECT `uuid`, `creatorId`, `categoryId`, `created_at`, `updated_at` FROM `creator_categories` AS `CreatorCategory` WHERE `CreatorCategory`.`categoryId` = 1;

Executing (default): DELETE FROM `creator_categories` WHERE `creatorId` = 59 AND `categoryId` = 1

Executing (default): DELETE FROM `creator_categories` WHERE `creatorId` = 105 AND `categoryId` = 1

Executing (default): SELECT `uuid`, `brandId`, `categoryId`, `updated_at`, `created_at` FROM `brand_categories` AS `BrandCategory` WHERE `BrandCategory`.`categoryId` = 1;

Executing (default): DELETE FROM `categories` WHERE `id` = 1
```