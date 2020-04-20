POSTGRESQL 12 Administration DBA Curriculum.

Introduction and Architectural Overview
History of PostgreSQL Major Features PPAS Features Architectural Overview General Database Limits Common Database Object Name


PostgreSQL System Architecture
Architectural Summary Process & Memory Architecture Utility Processes Connection Request-Response Disk Read Buffering Disk Write Buffering Background Writer Cleaning Scan Commit & Checkpoint Statement Processing Physical Database Architecture Data Directory Layout Installation Directory Layout Page Layout

Installation
OS User & Permissions Installation Options Installation of PostgreSQL Stack Builder Setting Environmental Variables OS User & Permissions Installation Options Installation of PostgreSQL Stack Builder Setting Environmental Variables


Database Clusters
Database Cluster Creating a Database Cluster Starting and Stopping the Server (pg_ctl) Connect to the Server Using psql


Configuration
Setting PostgreSQL Parameters Access Control Connection Settings Security and Authentication Settings Memory Settings Query Planner Settings WAL Settings

Log management
Background Writer Settings Statement Behaviour Configuration File Includes

Creating and Managing Databases
Object Hierarchy Creating Databases

Users
Access Control Creating Schemas Schema Search Path

User Tools: Command-Line Interfaces
Introduction to PSQL and EDB-PSQL

Conventions
Connecting to Database PSQL Command Line Parameters Entering PSQL Commands PSQL Meta-Commands PSQL SET Parameters Information Commands

GUI Tools - Intro to PGADMIN4 Introduction to PEM Client Registering a server Viewing and Editing Data Query Tool Databases Languages 
Schemas Database Objects Maintenance Table spaces Roles

Security Authentication and Authorization Levels of Security Pg_hba.conf File Object Ownership
Application Access Parameters Protecting Against Injection Attacks with SQL/Protect Source Code Protection for Functions

PG/SQL Data Types Structured Query Language (SQL) Tables and Constraints Manipulating Data using INSERT, UPDATE and DELETE Creating Other Database Objects: Sequences, Views, and Domains Table Partitioning Partitioning Partitioning Methods When to Partition Partitioning Setup Partitioning Example Partitioning and Constraint Exclusion Caveats

Introduction to various SQL functionalities Quoting SQL Functions Concatenation Nested Queries Joins Materialized Views Updatable Views o Indexes

Backup and Recovery & Point-in-Time Recovery Backup Types SQL Dump Backups SQL Dump Options Handling Large Databases Restoring SQL Dumps Cluster Dump Offline Backups Recovering a Database using Offline

Backups Online Directory Backups Continuous Archiving Backup with Low-level API How to use pg_base backup for Online Backups Point-In-Time Recovery Concepts Recovery Example Backup and Recovery Tool (BART)

Routine Maintenance Database Maintenance Maintenance Tools Optimizer Statistics Data Fragmentation Routine Vacuuming Vacuuming Commands
Preventing Transaction ID Wraparound Failures Vacuum Freeze The Visibility Map

Data Dictionary The System Catalogue Schema System Information Tables System Information Functions System Administration Functions System Information Views Oracle-like Dictionaries

Moving Data Loading flat files Import and export data using COPY Examples of COPY Command Using COPY FREEZE for performance Introduction to EDB*Loader for PPAS

SQL Tuning Statement Processing Common Query Performance Issues SQL Tuning Goals SQL Tuning Steps Identify slow queries Review the query execution plan Optimizer statistics and behaviour Restructure SQL statements Indexes

SQL Tuning continues...
Review Final Execution Plan
Performance Tuning Performance Tuning - Overview Performance Monitoring using PEM A-Tuning Technique Operating System Considerations Server Parameter Tuning Memory Parameters Temporary File Parameters WAL Parameters

Streaming Replication Data Replication Data Replication in PostgreSQL

Sync or ASync

Log-Shipping Standby Servers

Log-Shipping Architecture
Streaming Replication

Hot Streaming Architecture Cascading Replication Setup Replication Using Archive Setup Streaming Replication Prepare the Primary Server Synchronous Streaming Replication Setup Configure Authentication Take a Full Backup of Primary Server Setting up the Standby Server Adding Cascading Replicated Standby Server
Monitoring Hot Standby Recovery Control Functions

Connection Pooling
Connection Pooling Overview Pgpool-II – Features Connection pooling Replication Load balance Limiting exceeding connections Automatic failover Pgpool II - Installation and Configuration Configuring pcp.conf, pgpool.conf Setting up pool_hba.conf for Client Authentication (HBA) Starting/Stopping pgpool-II

Extension Modules What are Extension Modules? Installing Extension Modules Module Index Monitoring Database Monitoring Database Statistics The Statistics Collector Database Statistic Tables Operating System Process Monitoring Current Sessions and Locks Log Slow Running Queries Disk Usage PostgreSQL Enterprise Manager PEM – Features PEM – Architecture

Upgrading Best Practices Version Change and Upgrade Need to Upgrade Upgrade Plan Upgrade Using pg_upgrade Upgrading Best Practices
