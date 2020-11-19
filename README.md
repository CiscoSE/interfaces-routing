# Interfaces and routing package

This NSO package includes a service that configure interfaces ip addressing and OSPF routing protocol on a device. It accepts as input a list of Gigabit interfaces, OSPF process id and area

## Install

1. Clone this repo under the packages directory
2. cd to src and execute make clean all
3. Perform a packages reload in NSO

## Requisites
1. NSO 5.1 or greater 
2. python3
3. cisco-ios NED

## Configuration example

```

interfaces-routing csr-01-routing
 device csr-01
 interface 2
  ip_address 1.1.1.1
  netmask    255.255.255.0
 !
 interface 3
  ip_address 1.1.2.1
  netmask    255.255.255.0
 !
 ospf process 1
 ospf area 0
!
```

## Contacts

* Santiago Flores Kanter (sfloresk@cisco.com)