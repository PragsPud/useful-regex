---
layout: page
title: Commonly Used Regex Expressions
---

# Commonly Used Regex Expressions

Regular Expressions (Regex) are patterns used for searching, validating, and manipulating text. Below is a collection of the most commonly used regex expressions.

---

## **1. Digits**
- **Whole Numbers**: `/^\d+$/`
- **Decimal Numbers**: `/^\d*\.\d+$/`
- **Whole + Decimal Numbers**: `/^\d*(\.\d+)?$/`
- **Negative, Positive Whole + Decimal Numbers**: `/^-?\d*(\.\d+)?$/`
- **Whole + Decimal + Fractions**: `/[-]?[0-9]+[,.]?[0-9]*([\/][0-9]+[,.]?[0-9]*)*/`

---

## **2. Alphanumeric Characters**
- **Without Space**: `/^[a-zA-Z0-9]*$/`
- **With Space**: `/^[a-zA-Z0-9 ]*$/`

---

## **3. Email Validation**
- **Common Email IDs**: `/^([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6})*$/`
- **Uncommon Email IDs**: `/^([a-z0-9_\.\+-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

---

## **4. Password Strength**
 **Moderate Passwords**: `/(?=(.*[0-9]))((?=.*[A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z]))^.{8,}$/`

---

## **5. Username Validation**
Alphanumeric string that may include `_` and `-` with a length of 3 to 16 characters:
`/^[a-z0-9_-]{3,16}$/`

---

## **6. URL Validation**
- **Include Protocol (http/https)**: `/https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#()?&//=]*)/`
- **Protocol Optional**: `/(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/`

---

## **7. IP Address Validation**
**IPv4 Address**:  
  `/^(([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])\.){3}([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])$/`
  
---

## **8. Date Validation**
### Format Examples:
  `YYYY-MM-DD`: `/([12]\d{3}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01]))/`

---

## **9. HTML Tags**
Match HTML elements with attributes: `/<\/?[\w\s]*>|<.+[\W]>/`

---

## **10. Phone Numbers**
International format with optional country code or extension:
`/^(?:(?:\(?(?:00|\+)([1–4]\d\d|[1–9]\d?)\)?)?[\-\.\ \\\/]?)?((?:\(?\d{1,}\)?[\-\.\ \\\/]?){...})$/`

---
