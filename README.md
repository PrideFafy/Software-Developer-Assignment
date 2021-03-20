### Developer Task 1 

* You will receive instructions from Cassava Smartech on what's required.

##Fixes
1. Make LOGGER a static variable in MobileNumberUtils.java
2. Change @PreInsert to @PrePersist in SubscriberRequest.java
3. Change "select r from Request r where" to "select r from request r where" in SubscriberRequest.java
4. Remove this(super); from the PartnerCodeValidatorImpl constructor
5.  In CreditsServiceImpl.java (line 38) Change subscriberRequestDao.persist to subscriberRequestDao.save 
6. In CreditsServiceImpl.java (line 41) Change subscriberRequestDao.update to subscriberRequestDao.save
7. In EnquiriesServiceImpl.java (line 36) Change subscriberRequestDao.persist to subscriberRequestDao.save
8.  In EnquiriesServiceImpl.java (line 39) Change subscriberRequestDao.update to subscriberRequestDao.save
9. javax is no longer part of standard Java from 11+ so you have to manually add the dependencies 

### Fixing Integration Tests
1. ResponseCode.java change line 11 from [code = code;] to [this.code = code;] - there is a missing this.
2. In EpayResource.java on line 28 put  @PathVariable("partnerCode") before the final String pCode to binds the {partnerCode} variable in the url to the pCode local variable
