### Namespaces for Farm Data Identifiers

#### Purpose and Scope

The purpose of the urn:nzl:pri: namespace is to support a list of unique identifier namespaces for use within the primary sector. A variety of official biosecurity and genetic recording schemes define identifiers for farms, herds, organisations and animals. A master list of these schemes allows software and device vendors to understand and interpret identifiers in a useful manner.

The NZ Farm Data Standards project is the interim administrator of the urn:nzl:pri: namespace, delegated by the Department of Internal Affairs of the New Zealand Government, consistent with RFC-4350. It is charged with uniquely assigning the namespace at this level.

#### Structure

The identifier has a hierarchical structure as follows:

      urn:nzl:pri: nz-specifier>[:<nz-specifier defined string>]+

(+) denotes one or more occurrences of nz-specifier defined strings all delimited by a colon.

For example:     

* urn:nzl:pri:herd:tbfree:                 (e.g. 4071234)

* urn:nzl:pri::herd:nait:                    (e.g. 50812345) 

* urn:nzl:pri:animal:nait_traka:     (e.g. 982-000356154301-9999999)

* urn:nzl:pri:animal:nait_visual:    (e.g. 655123-13-258974)

The <nz-specifier> and <nz-specifier defined string> can comprise any UTF-8 characters compliant with URI syntax and must not contain the ":" character (see STD 66, RFC 3986).  The exclusion of the colon from the list of other characters means that the colon can only occur as a delimiter between string values.

#### Rules for Lexical Equivalence

The lexical equivalence of the NZL namespace-specific strings (NSSs) is defined as an exact, but not case-sensitive, string match.  Best Practice guidelines specify:

1. NZL in either uppercase or lowercase (Names will be assigned as case-insensitive, to ensure that there will not be two NZL URNs differing only by case.)

2. The first letter of the second word <nz-specifier> and <nz specifier defined string> in uppercase (camel case) or the whole value in lowercase.

3. Any identifier in NZL namespaces can be compared using the normal mechanisms for percent-encoded UTF-8 strings.

4. The use of diacritic marks such as Maori macrons in identifiers is supported as described in RFC-4350.

#### Registering your Namespace Identifier

Please contact the Declared Registrant of the urn:nzl:pri: namespace below to register additional identifier namespaces:

NZ Farm Data Standards
New Zealand

Use our [Contact page](https://github.com/Datalinker-Org/Datalinker-Org.io/blob/master/contact.md) to email us.

You will be required to supply your organisation contact details (address and email), proposed namespace, scope of identifiers (entities covered), and optionally a POSIX regular expression that provides initial parsing for the identifiers.

#### Existing Namespace Objects
Below are listed the existing Namespaces used primarily for the Animal Data Standards and DataLinker. Note that the processor URN is also included. 

Further classes can be proposed to the Declared Registrant of the urn:nzl:pri:namespace (contact details above). It is expected, for example, that plant specific classes may be added. 

Category | Identifier | URN	| Description | Format | Values | Owner
:------- | :--------- | :-- | :---------- | :----- | :----- | :----
Animal | TB Free Visual	| urn:nzl:pri:animal:id:tbfree_Visual | TBfree visual tags identify an animal suspected of having Tb, commonly referred to as the AHB rector tag.  This is always in addition to the management or NAIT tag.  This also includes an optional year code. Limited to Cattle and Deer herds. | "[AHB herd number]-[yy=year (optional)]-[sequence number], e.g. 5236512-12-123456 (hyphen to separate ID components) <br> Note that NAIT Visual Tag ID components should be separated by a hyphen (-)| TBfree_Visual (with year): aaaaaaa-yy-nnnnnn <br> Where a= AHB herd number  (7 digits) <br> y= year (2 digits) <br> n= sequence number (1-6 digits) |OSPRI New Zealand Limited info@nait.co.nz
Animal | NAIT Traka	| urn:nzl:pri:animal:id:nait_Traka | The NAIT Traka is a visual representation of RFID tag is used for Cattle and Deer born before 1/7/2012, though Traka tags were also used after NAIT was established. Scope also includes the TBfree or AHB Traka with the 7 digit TBFree number in place of the NAIT number. Note that the Manufacturer-code is aligned to ISO11785. Limited to Cattle and Deer herds.	| "The NAIT_Traka postfix can be up to 8 digits, but excluding 7 digits: [Manufacturer-Code ]-[number part of RFID]-[NAIT number {7}, e.g. 942-000012345123-258974 <br> TBfree Traka: [Manufacturer-Code]-[number part of RFID]-[TBfree herd number{7}, e.g.  982-523651-258974-1234567" | "NAIT_Traka: mmm-NNNNNNNNNNNN-AAAAAAAA <br> Tbfree Traka: : mmm-NNNNNNNNNNNN-aaaaaaa <br> Where m=ICAR manufacturer code <br> N= number part of RFID (12 digits) <br> A= NAIT number  (2-6 or 8 digits)<br> a= AHB herd number (7 digits) | OSPRI New Zealand Limited info@nait.co.nz
Animal | NAIT Visual | urn:nzl:pri:animal:id:nait_Visual | Visual RFID tag used as the official animal identifier for cattle and deer. NAIT Visual Tag IDs for birth ID formats should be unique, unless the tag is intended to replace a matching NAIT Visual Tag ID where the original tag has been damaged or lost. The NAIT Visual can also include the year born as optional. | "[NAIT number]-[yy(optional)]-[sequence number], e.g. 655123-13-258974, or 655123-258974 <br> Note that NAIT Visual Tag ID components should be separated by a hyphen (-) | "	"NAIT_Visual (with year): AAAAAA-yy-nnnnnn <br> Where A= NAIT number  (2-6 or 8 digits) <br> y= year (2 digits) <br> n= sequence number (1-6 digits)| "	"OSPRI New Zealand Limited info@nait.co.nz
Animal | SIL Official ID | urn:nzl:pri:animal:id:sil | "An official SIL identifier includes the flock code and tag (the latter a text string), and may optionally include the year born (by convention the year is often included in the tag number). | "	"[birthFlockCode].[yearBorn].[animalTag] |[ffff].[yyyy].[nnnnnnnnnnnnnnnnnnnnnnnnn] <br> f = birthFlockCode <br> y = yearBorn <br> n = animalTag | "Beef + Lamb Genetics Limited info@blnzgenetics.com"
Animal | ISO 11784 (RFID) | urn:iso:std:iso:11784 | An RFID tag is an ICAR coded radio frequency identification tag consisting of a 3 digit ICAR code and a unique 12 digit sequence number | [ICAR Manufacturer code] [unique sequence number] | "RFID: mmm nnnnnnnnnnnn  (space may be omitted) <br> where m = ICAR code <br> n = twelve digit unique sequence number <br> ICAR codes (NZ): <br> 982 – Allflex <br> 951 – Leader <br> 942 – Zee Tags | [International Standards Organisation](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.htm?csnumber=25881)
Animal | GS1 SGTIN (UHF RFID) | urn:epc:id:sgtin | Some trials with UHF RFID in deer  have used an SGTIN (Serialised Global Trade Item Number) issued by global standards organisation GS1 , which functions much like a barcode identifies a category of products, but with the addition of a unique item number as well. | | [GS1](http://www.gs1.org/epcglobal)
Herd | TB Free Number | urn:nzl:pri:herd:TBfree | "TBfree Herd number, sometimes referred to as the AHBHerd.  Defines the animals that live together as a group (for disease management purposes). Currently this is limited to Cattle and Deer herds. |  7 digits required, e.g.  4061234 | nnnnnnn where n= {0-9} | "OSPRI New Zealand Limited info@nait.co.nz
Herd | NAIT Number | urn:nzl:pri:herd:NAIT | Referred to as the NAIT number.  The number corresponds to a person in charge of animals (PICA) at a location where Cattle or Deer is produced. | Up to 8 digits (can be 2, 3, 4, 5, 6 or 8 digits, but not 7 digits), e.g.  50812345 | nnnnnnnn  where n={0-9} | "OSPRI New Zealand Limited info@nait.co.nz
Herd | Flock Code | urn:nzl:pri:herd:sil | Sheep Improvement Database Flock Code. Flock Code is used to define Birth Flock and to define Current Flock | Format: Four – five digit code where n={0-9} | "Beef + Lamb Genetics Limited info@blnzgenetics.com"
Observation	| Animal Observation | urn:nzl:pri:animal:observ | This object describes the definitions for individual observations or traits of a group or animal. | | "NZ Farm Data Standards info@datalinker.org.nz"
Location | Processor | urn:nzl:pri:processor | Processing plants. These are identifier codes used to describe a processing plant. | | "NZ Farm Data Standards info@datalinker.org.nz"
