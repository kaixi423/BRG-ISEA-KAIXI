Total Cost of Ownership (TCO) in Cloud Infrastructure
(Based on: TCO Analysis Lab for AWS vs Azure)

Session 2a: Total cost of ownership Lab: Total Cost of Ownership – Apply TCO concepts in practical comparison.

Compare cloud vs on-prem cost (hardware, software, licensing). 
For this task, I will be using Dell, AWS and Azure for comparison.
For Dell I choose the Dell PowerEdge T160, a tower server designed for small to medium businesses. 
https://www.dell.com/en-sg/shop/cty/pdp/spd/poweredge-t160/pet16010a 


<img width="450" height="250" alt="image" src="https://github.com/user-attachments/assets/f01f202f-c06f-40fa-b739-1a2cce061223" />



Below I have listed the specs I have chosen for the dell tower.
I did not choose a operating system as I will be using Ubuntu Linux Server Edition which is open source and has a $0 license fee. I will be using this OS for the cloud services to ensure that my comparison is fair. 


<img width="448" height="600" alt="image" src="https://github.com/user-attachments/assets/6456e93d-4b68-46a8-9b8e-9f4c63712fe5" />

<img width="459" height="598" alt="image" src="https://github.com/user-attachments/assets/afbc6b10-8bab-469c-a616-c6a63e09eb21" />

<img width="405" height="569" alt="image" src="https://github.com/user-attachments/assets/b379f69e-3217-4460-8d5c-9b5320b0f982" />

 
I will be estimating $15 per month for electricity, cooling and possible battery wear over 3 years. I will be calculating 15x12 = 180 for 1 years cost and multiplying it by 3 to calculate the amount for 3 years which would lead to $540. I will be adding this $540 to the upfront cost to purchase the hardware (4104.04) which is $4644.04.
The 3 year TCO (Total cost of ownership) of owning your own on-premises server is $4644.04.








For Azure Cloud options, I will be choosing the Standard-B1s Virtual machine.
I have listed the specifications below:

<img width="581" height="258" alt="image" src="https://github.com/user-attachments/assets/663b679a-05f9-4306-977f-005c6eace09b" />

<img width="514" height="468" alt="image" src="https://github.com/user-attachments/assets/4709b296-542b-4ee4-a128-0cc3f16ce669" />

<img width="517" height="286" alt="image" src="https://github.com/user-attachments/assets/aae1fccd-68c8-46e0-a86e-42a330bc020d" />

<img width="578" height="257" alt="image" src="https://github.com/user-attachments/assets/0346a3f0-3f47-4b6b-bfc1-3ee2979ae929" />

<img width="574" height="344" alt="image" src="https://github.com/user-attachments/assets/90232362-40c2-4623-871c-3a1a86dd4999" />

<img width="513" height="275" alt="image" src="https://github.com/user-attachments/assets/f39d691c-90f4-4c81-87a2-75d476fc7200" />





The baseline Azure Standard_B1s compute instance runs at an unmanaged rate of US$7.59/month. To create a functioning server environment, a 32 GiB managed boot volume (~S$2.20/mo) is added to the operational parameters, bringing the functional runtime entry point to roughly S$10–S$12.30/month.
I will be taking the higher end of the price to manage this cloud for comparison. 
12.30x36=442.8
The TCO for Azure cloud is $442.8 by year 3.

For AWS Cloud services, I will be choosing Amazon EC2 t2.micro instance.
I have listed the specifications below. 


<img width="886" height="293" alt="image" src="https://github.com/user-attachments/assets/e1e778fa-0c6f-434d-a39e-68c67df724bf" />

 
(I took the on-demand price/hr instead of their reserved instance effective hourly to ensure the comparison is as accurate as possible.)
The baseline hourly rate for an AWS EC2 t2.micro instance running ubuntu is US$0.0116 per hour. Which is USD$8.47 Per month which is around S$11.30/month.
I added a operating system storage volume of 32GiB gp3 block volume which is around S$3.50/month. So the total cost of running this server would be S$14.80 per month. Which means that the total cost of running this server would be S$532.80 for 3 years.
The TCO for AWS Cloud services is $532.80 for 3 years.




I have documented monthly and yearly costs here.


<img width="706" height="325" alt="image" src="https://github.com/user-attachments/assets/ab3737bd-8e55-4ace-9836-e32a7dd7b3c6" />

Calculating ROI Metrics:
To calculate the ROI metric I will use the total cost of 3 Year cumulative cloud cost minus 3 year on prem TCO divided by initial upfront on prem capital expenditure and  multiply it by 100. 

Dell Poweredge T160 vs. Azure Cloud (Standard_B1s)
This metric calculates the return of investing in a local physical server instead of subscribing to Azure over a 3-year timeline.
•	Initial Upfront Investment (Dell CapEx): S$4,104.04
•	3-Year Total Cost of Baseline Alternative (Azure TCO): S$442.80
•	3-Year Total Cost of Selected Option (Dell TCO): S$4,644.04


<img width="539" height="244" alt="image" src="https://github.com/user-attachments/assets/b903b5db-5f33-4824-887f-6eb0757fc91b" />


 



What this actually means:
Because the ongoing local utility power overhead to keep the physical server online (S$15/mo) is higher than the entire Azure monthly subscription (S$12.30/mo), there are no monthly operational savings. The physical server can never break even, resulting in a complete loss of capital efficiency (-102.4% ROI) over the 3-year track.

Dell PowerEdge T160 vs. AWS Cloud (t2.micro)
This metric calculates the return of investing in a local physical server instead of subscribing to AWS over a 3-year timeline.
•	Initial Upfront Investment (Dell CapEx): S$4,104.04
•	3-Year Total Cost of Baseline Alternative (AWS TCO): S$532.80
•	3-Year Total Cost of Selected Option (Dell TCO): S$4,644.04


<img width="489" height="222" alt="image" src="https://github.com/user-attachments/assets/e4ce94f7-9948-4553-8196-3af16590a2e0" />

What this actually means:
Similar to the Azure scenario, local utility run rates exceed the AWS subscription cost by S$0.20 per month, preventing an operational savings threshold from ever being achieved. The upfront Capital Expenditure premium results in a negative financial yield (-100.2% ROI).

Azure Cloud (Standard_B1s) vs. AWS Cloud (t2.micro)
This metric fulfills your assignment prompt to "Compare TCO across cloud providers." It evaluates the financial yield of selecting Azure instead of AWS Because both options are pure operating expenses with S$0.00 upfront costs, financial standards use the total 3-year AWS alternative cost as the denominator.
•	3-Year Total Cost of Baseline Alternative (AWS TCO): S$532.80
•	3-Year Total Cost of Selected Option (Azure TCO): S$442.80
•	Initial Upfront Investment: S$0.00 (Pure Operational Cost comparison)


<img width="636" height="206" alt="image" src="https://github.com/user-attachments/assets/fe74128c-6f9d-4d50-88c3-aace767425d5" />

 
What this actually means:
Under a standard on-demand model, Azure is cheaper than AWS from Day 1 onwards (S$12.30 vs S$14.80). Because Azure carries S$0.00 upfront and is cheaper every subsequent month, AWS will never hit a threshold to cross over or break even against Azure's TCO. Choosing Azure saves the business a flat S$90.00 over three years, improving infrastructure budget efficiency by +16.9%.

From these results:
1.	Hardware vs. Micro-Cloud TCO Imbalance:
Both hardware-to-cloud scenarios display a negative return on investment (~ -100%). From a strict financial perspective, dedicating S$4,104.04 of upfront capital to run a task small enough to fit within an entry-level 1GB RAM cloud slice is highly inefficient. The local utility power overheads alone surpass the monthly cost of a micro cloud instance.

2.	Cross-Cloud Provider Efficiency Winner:
Comparing the cloud hyperscalers directly reveals that Azure yields a +16.9% ROI advantage over AWS. While both platforms offer identical basic hardware allocations (1 vCPU, 1GB RAM), Azure's localized Southeast Asia region rates for compute runtime and standard storage are lower than AWS's legacy t2.micro pricing structure. This saves the business a flat S$90.00 over 36 months.


Architectural Disclaimer: Peformance and resource imbalance.
When analyzing the 3-year TCO metrics, the financial calculations heavily favor the public cloud providers due to a massive, deliberate mismatch in hardware resource scales. This comparison matches a heavy, physical on-premises server against the absolute smallest entry-tier virtual machines available in the cloud:
1.	The Processing & Memory Gap: The on-premises Dell PowerEdge T160 features a dedicated physical processor and 16 GB of DDR5 RAM. In stark contrast, the Azure B1s and AWS t2.micro instances only allocate a tiny slice of shared hardware containing 1 GB of RAM. A 1 GB virtual machine is highly restricted and would frequently crash or freeze if tasked with running production-grade corporate databases, heavy local file transfers, or modern business applications.
2.	The Storage Discrepancy: The physical Dell server includes a massive 2,000 GB (2 TB) local hard drive built directly into its system. The baseline Azure and AWS configurations only include a tiny 32 GB boot disk to hold the basic operating system.
