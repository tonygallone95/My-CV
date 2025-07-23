<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Antony Gallone - CV</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.6;
            color: #1a1a1a;
            background: #ffffff;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 20px rgba(0,0,0,0.05);
        }
        
        /* Header Section */
        .header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 50px 60px 40px;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 500px;
            height: 500px;
            background: rgba(255,255,255,0.05);
            border-radius: 50%;
        }
        
        .header h1 {
            font-size: 42px;
            font-weight: 700;
            margin-bottom: 8px;
            letter-spacing: -0.5px;
        }
        
        .header .title {
            font-size: 18px;
            font-weight: 300;
            opacity: 0.9;
            margin-bottom: 25px;
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            font-size: 14px;
            position: relative;
            z-index: 1;
        }
        
        .contact-info span {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        /* Main Content */
        .content {
            padding: 50px 60px;
        }
        
        /* Section Styles */
        .section {
            margin-bottom: 45px;
        }
        
        .section-title {
            font-size: 24px;
            font-weight: 700;
            color: #1e3c72;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #e8f0fe;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 60px;
            height: 3px;
            background: #2a5298;
        }
        
        /* Summary */
        .summary {
            font-size: 15px;
            color: #444;
            line-height: 1.8;
            background: #f8f9fa;
            padding: 25px;
            border-radius: 8px;
            border-left: 4px solid #2a5298;
        }
        
        /* Skills Table */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }
        
        .skill-card {
            background: #ffffff;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            padding: 20px;
            transition: all 0.3s ease;
        }
        
        .skill-card:hover {
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            transform: translateY(-2px);
        }
        
        .skill-category {
            font-size: 16px;
            font-weight: 600;
            color: #1e3c72;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }
        
        .skill-tag {
            background: #e8f0fe;
            color: #2a5298;
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 500;
        }
        
        /* Experience */
        .experience-item {
            margin-bottom: 35px;
            padding: 25px;
            background: #fafbfc;
            border-radius: 8px;
            border-left: 4px solid #2a5298;
            position: relative;
        }
        
        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 15px;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .job-title {
            font-size: 20px;
            font-weight: 600;
            color: #1a1a1a;
        }
        
        .company {
            font-size: 16px;
            color: #2a5298;
            font-weight: 500;
        }
        
        .date {
            font-size: 14px;
            color: #666;
            background: #e8f0fe;
            padding: 4px 12px;
            border-radius: 20px;
        }
        
        .achievement {
            margin-top: 15px;
            padding: 15px;
            background: white;
            border-radius: 6px;
            border: 1px solid #e0e0e0;
        }
        
        .achievement-metric {
            font-weight: 600;
            color: #1e3c72;
            font-size: 16px;
            margin-bottom: 8px;
        }
        
        .tech-stack {
            margin-top: 10px;
            font-size: 13px;
            color: #666;
        }
        
        .tech-stack strong {
            color: #2a5298;
        }
        
        /* Certifications */
        .cert-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .cert-item {
            background: #f8f9fa;
            padding: 15px 20px;
            border-radius: 6px;
            border-left: 3px solid #2a5298;
            font-size: 14px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .cert-icon {
            width: 20px;
            height: 20px;
            background: #2a5298;
            border-radius: 50%;
            flex-shrink: 0;
        }
        
        /* Icons */
        .icon {
            width: 18px;
            height: 18px;
            fill: currentColor;
        }
        
        /* Print Styles */
        @media print {
            body {
                background: white;
            }
            .container {
                box-shadow: none;
            }
            .experience-item {
                break-inside: avoid;
            }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header, .content {
                padding: 30px;
            }
            .header h1 {
                font-size: 32px;
            }
            .contact-info {
                font-size: 12px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>Antony Gallone</h1>
            <div class="title">Application Support Consultant | Technical Operations Engineer</div>
            <div class="contact-info">
                <span>
                    <svg class="icon" viewBox="0 0 24 24">
                        <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7z"/>
                        <circle cx="12" cy="9" r="2.5"/>
                    </svg>
                    Leeds, UK
                </span>
                <span>
                    <svg class="icon" viewBox="0 0 24 24">
                        <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
                    </svg>
                    tgallone95@outlook.com
                </span>
                <span>
                    <svg class="icon" viewBox="0 0 24 24">
                        <path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/>
                    </svg>
                    07783 181 677
                </span>
                <span>
                    <svg class="icon" viewBox="0 0 24 24">
                        <path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/>
                    </svg>
                    linkedin.com/in/tonygallone288424a7
                </span>
            </div>
        </div>
        
        <!-- Content -->
        <div class="content">
            <!-- Summary -->
            <div class="section">
                <h2 class="section-title">Professional Summary</h2>
                <div class="summary">
                    Application Support Consultant with 15 years of experience specializing in cloud infrastructure, DevOps automation, and high-performance database systems. Expert in transforming underperforming operations into efficient, scalable solutions across AWS and Azure environments. Proven track record of delivering significant cost savings, improving system reliability, and leading technical teams through complex migrations and optimizations.
                </div>
            </div>
            
            <!-- Skills -->
            <div class="section">
                <h2 class="section-title">Technical Expertise</h2>
                <div class="skills-grid">
                    <div class="skill-card">
                        <div class="skill-category">☁️ AWS Cloud</div>
                        <div class="skill-tags">
                            <span class="skill-tag">EC2</span>
                            <span class="skill-tag">Lambda</span>
                            <span class="skill-tag">ECS</span>
                            <span class="skill-tag">S3</span>
                            <span class="skill-tag">RDS</span>
                            <span class="skill-tag">DynamoDB</span>
                            <span class="skill-tag">Aurora</span>
                            <span class="skill-tag">VPC</span>
                            <span class="skill-tag">CloudWatch</span>
                            <span class="skill-tag">CloudFormation</span>
                            <span class="skill-tag">Kinesis</span>
                            <span class="skill-tag">API Gateway</span>
                        </div>
                    </div>
                    
                    <div class="skill-card">
                        <div class="skill-category">☁️ Azure Cloud</div>
                        <div class="skill-tags">
                            <span class="skill-tag">Virtual Machines</span>
                            <span class="skill-tag">App Service</span>
                            <span class="skill-tag">Functions</span>
                            <span class="skill-tag">SQL Database</span>
                            <span class="skill-tag">Cosmos DB</span>
                            <span class="skill-tag">Monitor</span>
                            <span class="skill-tag">DevOps</span>
                            <span class="skill-tag">Logic Apps</span>
                            <span class="skill-tag">Data Factory</span>
                        </div>
                    </div>
                    
                    <div class="skill-card">
                        <div class="skill-category">🛠️ DevOps & Automation</div>
                        <div class="skill-tags">
                            <span class="skill-tag">Terraform</span>
                            <span class="skill-tag">Ansible</span>
                            <span class="skill-tag">Jenkins</span>
                            <span class="skill-tag">GitLab CI</span>
                            <span class="skill-tag">Docker</span>
                            <span class="skill-tag">Kubernetes</span>
                            <span class="skill-tag">ArgoCD</span>
                            <span class="skill-tag">CircleCI</span>
                            <span class="skill-tag">GitOps</span>
                        </div>
                    </div>
                    
                    <div class="skill-card">
                        <div class="skill-category">📊 Data & Languages</div>
                        <div class="skill-tags">
                            <span class="skill-tag">SQL Server</span>
                            <span class="skill-tag">PostgreSQL</span>
                            <span class="skill-tag">MySQL</span>
                            <span class="skill-tag">Python</span>
                            <span class="skill-tag">Bash</span>
                            <span class="skill-tag">PowerShell</span>
                            <span class="skill-tag">KQL</span>
                            <span class="skill-tag">SSIS</span>
                            <span class="skill-tag">Power BI</span>
                        </div>
                    </div>
                    
                    <div class="skill-card">
                        <div class="skill-category">📈 Monitoring & APM</div>
                        <div class="skill-tags">
                            <span class="skill-tag">Datadog</span>
                            <span class="skill-tag">Grafana</span>
                            <span class="skill-tag">Prometheus</span>
                            <span class="skill-tag">ELK Stack</span>
                            <span class="skill-tag">AppDynamics</span>
                            <span class="skill-tag">NewRelic</span>
                            <span class="skill-tag">PagerDuty</span>
                            <span class="skill-tag">ServiceNow</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Experience -->
            <div class="section">
                <h2 class="section-title">Professional Experience</h2>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">Consultant</div>
                            <div class="company">Burendo</div>
                        </div>
                        <div class="date">Feb 2025 – Present</div>
                    </div>
                    <div class="achievement">
                        <div class="achievement-metric">Transformed SLA compliance from 83% to 100% in 2 weeks</div>
                        <div>Achieved through predictive monitoring using KQL in Azure Monitor, Python-based Lambda auto-remediation, and integrated alerting via CloudWatch, Grafana, and PagerDuty. Built L2 support team utilizing GitOps with ArgoCD, automated infrastructure deployments through Terraform, and streamlined incident management via ServiceNow integration.</div>
                        <div class="tech-stack"><strong>Tech Stack:</strong> Azure Monitor, KQL, AWS Lambda, Python, CloudWatch, Grafana, PagerDuty, ArgoCD, Terraform, ServiceNow</div>
                    </div>
                </div>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">Technical Operations Engineer</div>
                            <div class="company">ENSEK</div>
                        </div>
                        <div class="date">Oct 2022 – Feb 2025</div>
                    </div>
                    <div class="achievement">
                        <div class="achievement-metric">Scaled infrastructure from 200K to 6M+ users | Saved £150K/month</div>
                        <div>Successfully executed comprehensive AWS migration deploying Multi-AZ Aurora clusters for database resilience and Kinesis Analytics processing 10M+ events daily. Achieved significant cost savings through Reserved Instances and Spot Fleet optimization. Automated infrastructure using Terraform and CloudFormation while maintaining real-time monitoring through Datadog and CloudWatch.</div>
                        <div class="tech-stack"><strong>Tech Stack:</strong> AWS (Aurora, Kinesis, EC2), Terraform, CloudFormation, Datadog, CloudWatch, Reserved Instances, Spot Fleet</div>
                    </div>
                </div>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">Technical Operations Engineer</div>
                            <div class="company">TheDataShed</div>
                        </div>
                        <div class="date">Feb 2021 – Oct 2022</div>
                    </div>
                    <div class="achievement">
                        <div class="achievement-metric">Reduced SQL query execution time by 75% | Prevented £2M in SLA penalties</div>
                        <div>Optimized performance across 50+ SQL Server databases by implementing columnstore indexes for analytics, strategic data partitioning for large tables, and Always On Availability Groups for enhanced reliability. Provided L3 support handling complex escalations and root cause analysis.</div>
                        <div class="tech-stack"><strong>Tech Stack:</strong> SQL Server, Columnstore Indexes, Always On AG, Data Partitioning, Performance Tuning</div>
                    </div>
                </div>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">SQL/Application Developer</div>
                            <div class="company">Communisis</div>
                        </div>
                        <div class="date">Nov 2017 – Apr 2020</div>
                    </div>
                    <div class="achievement">
                        <div class="achievement-metric">Cut report generation from 6 hours to 45 minutes | £3M revenue impact</div>
                        <div>Efficiently processed 5M+ records daily by designing parallelized SSIS packages integrated with Azure Data Factory, enabling real-time analytics. The optimization directly contributed to significant revenue increases through faster business insights and decision-making capabilities.</div>
                        <div class="tech-stack"><strong>Tech Stack:</strong> SSIS, Azure Data Factory, Power BI, Azure Synapse Analytics, T-SQL</div>
                    </div>
                </div>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">Database Administrator</div>
                            <div class="company">MotorMile Finance</div>
                        </div>
                        <div class="date">Mar 2016 – Oct 2017</div>
                    </div>
                    <div class="achievement">
                        <div class="achievement-metric">Improved response time by 80% | Saved £500K annually</div>
                        <div>Revolutionized call center operations supporting 500+ agents through automated ETL processes using Python and SQL Agent. Optimized 200+ stored procedures and critical reports, dramatically improving user experience and operational efficiency.</div>
                        <div class="tech-stack"><strong>Tech Stack:</strong> SQL Server, Python, SQL Agent, ETL, Stored Procedures</div>
                    </div>
                </div>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">Junior Database Administrator</div>
                            <div class="company">Claritas Solutions</div>
                        </div>
                        <div class="date">Feb 2014 – Oct 2017</div>
                    </div>
                    <div class="achievement">
                        <div class="achievement-metric">Maintained 99.9% uptime for mission-critical databases</div>
                        <div>Implemented comprehensive backup strategies, disaster recovery procedures, and proactive monitoring. Developed index maintenance plans and performance monitoring using SQL Profiler and DMVs while supporting senior DBAs in complex tuning initiatives.</div>
                        <div class="tech-stack"><strong>Tech Stack:</strong> SQL Server, SQL Profiler, DMVs, Backup/Recovery, Index Optimization</div>
                    </div>
                </div>
            </div>
            
            <!-- Certifications -->
            <div class="section">
                <h2 class="section-title">Certifications</h2>
                <div class="cert-grid">
                    <div class="cert-item">
                        <div class="cert-icon"></div>
                        Microsoft Certified: Azure Data Engineer Associate
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon"></div>
                        Microsoft Certified: Data Analyst Associate
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon"></div>
                        Microsoft Certified: Azure Database Administrator Associate
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon"></div>
                        Microsoft Certified: Azure Fundamentals
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon"></div>
                        AWS Certified Cloud Practitioner
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon"></div>
                        AWS Certified Developer – Associate
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>