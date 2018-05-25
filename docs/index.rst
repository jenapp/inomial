.. Smile documentation master file, created by
   sphinx-quickstart on Mon Apr 30 15:35:19 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Smile's GraphQL API documentation!
=================================

.. toctree::
   :caption: GraphQL
   :hidden:
   
   graphql/graphql-intro
   graphql/resources

   
.. toctree::
   :caption: Schema
   :hidden:
   :maxdepth: 1
   
   Query <graphql/schema/query>
  

.. toctree::
   :caption: Scalars
   :hidden:
   
   BigDecimal <graphql/scalars/bigdecimal>
   Boolean <graphql/scalars/boolean>
   Int <graphql/scalars/int>
   Long <graphql/scalars/long>
   Milliseconds <graphql/scalars/milliseconds>
   String <graphql/scalars/string>
   UUID <graphql/scalars/uuid>


.. toctree::
   :caption: Enums
   :hidden:
   
   __DirectiveLocation <graphql/enums/directivelocation>
   __TypeKind <graphql/enums/typekind>


.. toctree::
   :caption: Objects
   :hidden:
   
   Account <graphql/objects/account>
   AccountAddress <graphql/objects/accountaddress>
   AccountContact <graphql/objects/accountcontact>
   AccountCostCentre <graphql/objects/accountcostcentre>
   AllAccountCursor <graphql/objects/allaccountcursor>
   AllDraftInvoiceCursor <graphql/objects/alldraftinvoicecursor>
   AllInvoiceItemCursor <graphql/objects/allinvoiceitemcursor>
   AllPlanCursor <graphql/objects/allplancursor>
   AllSubscriptionCursor <graphql/objects/allsubscriptioncursor>
   AllTicketCursor <graphql/objects/allticketcursor>
   Binding <graphql/objects/binding>
   BindingCursor <graphql/objects/bindingcursor>
   Cdr <graphql/objects/cdr>
   CdrCursor <graphql/objects/cdrcursor>
   CdrError <graphql/objects/cdrerror>
   DraftInvoice <graphql/objects/draftinvoice>
   ItemSpecification <graphql/objects/itemspecification>
   PaymentMethod <graphql/objects/paymentmethod>
   Plan <graphql/objects/plan>
   SearchResult <graphql/objects/searchresult>
   Service <graphql/objects/service>
   Subscription <graphql/objects/subscription>
   SubscriptionBinding <graphql/objects/subscriptionbinding>
   SubscriptionBindingCursor <graphql/objects/aubscriptionbindingcursor>
   SubscriptionCursor <graphql/objects/subscriptioncursor>
   TariffType <graphql/objects/tarifftype>
   Ticket <graphql/objects/ticket>
   TicketCursor <graphql/objects/ticketcursor> 
   Tx <graphql/objects/tx> 
   TxDetail <graphql/objects/txdetail>
   TxItem <graphql/objects/txitem>           
   TxItemCursor <graphql/objects/txitemcursor>           
   Ucdr <graphql/objects/ucdr>            
   UnbilledChargeSummary <graphql/objects/unbilledchargesummary>
   __Directive <graphql/objects/directive>
   __EnumValue <graphql/objects/enumvalue>
   __Field <graphql/objects/field>
   __InputValue <graphql/objects/inputvalue>
   __Schema <graphql/objects/schema>
   __Type <graphql/objects/type>


.. toctree::
   :caption: Input objects
   :hidden:
   
   AccountAddressFilter <graphql/inputobjects/accountaddressfilter>
   AccountContactFilter <graphql/inputobjects/accountcontactfilter>
   AccountCostCentreFilter <graphql/inputobjects/accountcostcentrefilter>
   AccountFilter <graphql/inputobjects/accountfilter>      
   BindingFilter <graphql/inputobjects/bindingfilter>
   CdrErrorFilter <graphql/inputobjects/cdrerrorfilter> 
   CdrFilter<graphql/inputobjects/cdrfilter>
   DraftInvoiceFilter <graphql/inputobjects/draftinvoicefilter>
   ItemSpecificationFilter <graphql/inputobjects/itemspecificationfilter>
   PaymentMethodFilter <graphql/inputobjects/paymentmethodfilter>
   PlanFilter <graphql/inputobjects/planfilter>
   ServiceFilter <graphql/inputobjects/servicefilter>
   SubscriptionBindingFilter <graphql/inputobjects/subscriptionbindingfilter>
   SubscriptionFilter <graphql/inputobjects/subscriptionfilter>
   TariffTypeFilter <graphql/inputobjects/tarifftypefilter>
   TicketFilter <graphql/inputobjects/ticketfilter>
   TxDetailFilter <graphql/inputobjects/txdetailfilter>
   TxFilter <graphql/inputobjects/txfilter>
   TxItemFilter <graphql/inputobjects/txitemfilter>
   
   
.. toctree::
   :caption: Directives
   :hidden:
   
   include <graphql/directives/include>
   skip <graphql/directives/skip>
      
   
.. toctree::
   :caption: REST APIs
   :hidden:
   
   apis/create
   apis/account
   apis/subscription




.. Indices and tables
   ==================

   * :ref:`genindex`
   * :ref:`modindex`
   * :ref:`search`
