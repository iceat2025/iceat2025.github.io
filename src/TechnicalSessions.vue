<script setup>
import { ref } from "vue";
import Main from "./Main.vue"
import Qrcode from "qrcode.vue"
import ImgRegister from "./assets/1.register.png"
import ImgParticipants from "./assets/2.participants.png"
import ImgConfirmation from "./assets/3.confirmation.png"
import ImgEmail from "./assets/4.email.png"
import ImgEventJoinPage from "./assets/5.event-join-page.png"
import ImgEventJoiningDetails from "./assets/6.event-joining-details.png"

const sessions = ref([
  {
    "name": "Physical Session (LT7)",
    "date": "23 July, 2025",
    "time": "14:00 - 16:30",
    // "qrdata": "Sunway University LT7",
    "papers": [
      {
        "id": 4,
        "title": "Ozone-Based Advanced Oxidation Processes for Dye Removal: A Brief Review",
        "time": "14:00 - 14:15"
      },
      {
        "id": 50,
        "title": "Numerical Investigation about Diesel Engine Powered by Waste Plastic Oil Blends under Different Load and Engine Speed",
        "time": "14:15 - 14:30"
      },
      {
        "id": 117,
        "title": "A Metal-Free Electrocatalyst for Efficient Hydrogen Production",
        "time": "14:30 - 14:45"
      },
      {
        "id": 118,
        "title": "Development and Optimization of Recyclable GF-reinforced PLA Resin Composite for Renewable Energy Applications ",
        "time": "14:45 - 15:00"
      },
      {
        "id": 120,
        "title": "   Bibliometric Analysis on Smart Self-Healing Nanocoating for 316L Stainless Steel Biomedical Implants ",
        "time": "15:00 - 15:15"
      },
      {
        "id": 127,
        "title": "   Effective Removal of Amoxicillin from Medical Wastewater Using an Eco-Friendly Modification of a Walnut Shell as an Adsorbent ",
        "time": "15:30 - 15:45"
      },
      {
        "id": 132,
        "title": "Experimental and Computational Evaluation of Graphene-Enhanced Fiberglass/Polyester Nanocomposites",
        "time": "15:45 - 16:00"
      },
      {
        "id": 155,
        "title": "Buckling Analysis of Corrugated Plate Fuselage Under Uniform Pressure Loading Condition ",
        "time": "16:00 - 16:15"
      },
      {
        "id": 180,
        "title": "Application of Kaplan Meier estimator model for validation of AURKC as an early biomarker for Kidney Cancer ",
        "time": "16:15 - 16:30"
      }
    ]
  },
  {
    "name": "Technical Session 1: Functional Materials and Nanotechnology in Chemical Engineering",
    "date": "23 July, 2025",
    "time": "10:00 - 12:00",
    "qrdata": "https://events.teams.microsoft.com/event/9e8379da-cfbd-473e-ab23-69960c2fdb9e@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 20,
        "title": "Improv\u0131ng The Propert\u0131es Of Thermoplast\u0131c Mater\u0131als Us\u0131ng Polyester Res\u0131n  W\u0131th Nanopart\u0131cles: The State-Of-The-Art",
        "time": "10:00 - 10:15"
      },
      {
        "id": 45,
        "title": "A Review of Novel Nanocomposite Adsorbents for Ultra-Deep Desulfurization of Diesel Fuel: Recent Advances and Future Perspectives",
        "time": "10:15 - 10:30"
      },
      {
        "id": 119,
        "title": "Impact  of Nanomaterials Concentrations  on the Stress\u2013Strain Behavior and Elastic Modulus of Resin Coatings under an Applied Load ",
        "time": "10:30 - 10:45"
      },
      {
        "id": 130,
        "title": "Optimization of CO\u2082-Assisted Gravity Drainage Operational Parameters: Insights from a 2D Hele-Shaw Model ",
        "time": "10:45 - 11:00"
      },
      {
        "id": 168,
        "title": "Characterization and Properties of Reaction Majnoon Field rock stone with Carbon Dioxide",
        "time": "11:00 - 11:15"
      },
      {
        "id": 175,
        "title": "Advanced Multiple Sclerosis Data Analysis Using Intensity-Guided Skull Removal and Level Set Method for Enhanced Accuracy",
        "time": "11:30 - 11:45"
      },
      {
        "id": 205,
        "title": "A comprehensive overview of carbon dioxide separation technologies for post-combustion capture ",
        "time": "11:45 - 12:00"
      }
    ]
  },
  {
    "name": "Technical Session 2: Intelligent Power and Communication Systems for Smart Infrastructure",
    "date": "23 July, 2025",
    "time": "10:00 - 12:15",
    "qrdata": "https://events.teams.microsoft.com/event/74c15f61-c757-496d-a713-230df9a591ab@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 8,
        "title": "Three-Phase Seventeen-Level Cascaded Switched-Capacitor Multilevel Inverter for Grid-Connected PV Systems",
        "time": "10:00 - 10:15"
      },
      {
        "id": 177,
        "title": "Safety-Oriented Design and Analysis of Dielectric Materials and Plate Geometry in Capacitive Wireless Power Transfer Systems",
        "time": "10:15 - 10:30"
      },
      {
        "id": 47,
        "title": "Adaptive Algorithm for Transmission Images in 3D LTE Wireless Communication System Channel Based on MIMO-OFDM",
        "time": "10:30 - 10:45"
      },
      {
        "id": 34,
        "title": "A High-Performance, Low-Cost Solution for Enhancing Capacity in Urban 5G Small Cells",
        "time": "10:45 - 11:00"
      },
      {
        "id": 166,
        "title": "Design and Implementation of a Reconfigurable Dual Band Low Noise Amplifier for Modern Receiving Systems ",
        "time": "11:00 - 11:15"
      },
      {
        "id": 112,
        "title": "Band Pass Filter Utilizing a Stepped Impedance Resonator for Modern Wireless Communication System ",
        "time": "11:30 - 11:45"
      },
      {
        "id": 29,
        "title": "Investigation of Near Field Distributions of Meander Line Antenna in Human Body Conditions",
        "time": "11:45 - 12:00"
      },
      {
        "id": 200,
        "title": "Bit Error Rate Analysis of Adaptive Modulation Techniques in Power Line Communication Channels",
        "time": "12:00 - 12:15"
      }
    ]
  },
  {
    "name": "Technical Session 3: Composite Materials, Structural Mechanics, and Manufacturing Innovations",
    "date": "23 July, 2025",
    "time": "10:00 - 12:15",
    "qrdata": "https://events.teams.microsoft.com/event/a36c6851-6d53-44e1-953e-bc242cf1a439@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 170,
        "title": "   A Review of Origami Structure According to Pattern, Manufacturing and Application ",
        "time": "10:00 - 10:15"
      },
      {
        "id": 161,
        "title": "Study The Effect of Tw\u0131n W\u0131re Arc Spray\u0131ng Parameters on Surface Propert\u0131es of Sta\u0131nless Steel  ",
        "time": "10:15 - 10:30"
      },
      {
        "id": 154,
        "title": "An Analytical Review of Incremental Single Sheet Metal Forming Techniques  ",
        "time": "10:30 - 10:45"
      },
      {
        "id": 150,
        "title": "Numerical analysis of multi \u2013layer composite under free vibration conditions",
        "time": "10:45 - 11:00"
      },
      {
        "id": 144,
        "title": "Effect of blades shape and duct geometrical parameters on Aerodynamic performance of a small-sized axial fan ",
        "time": "11:00 - 11:15"
      },
      {
        "id": 109,
        "title": "Effect of Nano Silica Fillers on Dynamic Mechanical Performance and Accelerated Ageing Behavior of Carbon/Epoxy Composites ",
        "time": "11:30 - 11:45"
      },
      {
        "id": 191,
        "title": "Designing a Structured Simulation and Project Based Learning Spine for Mechanical Engineering Education ",
        "time": "11:45 - 12:00"
      },
      {
        "id": 213,
        "title": "Experimental Determination of the Influence of Perforation of Adherend to the adhesive bond strength",
        "time": "12:00 - 12:15"
      }
    ]
  },
  {
    "name": "Technical Session 4: AI-Driven Intelligent Systems for Cybersecurity, Healthcare, and Smart Infrastructure",
    "date": "23 July, 2025",
    "time": "14:00 - 16:45",
    "qrdata": "https://events.teams.microsoft.com/event/f841b318-f93f-459b-b45e-09d597adbd9c@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 10,
        "title": "Optimizing Operating Room Scheduling Using Artificial Bee Colony and Bat Algorithm: A Comparative Analysis ",
        "time": "14:00 - 14:15"
      },
      {
        "id": 25,
        "title": "SmartSARIMAX: An Advanced Model for Bandwidth Prediction in Data Networks",
        "time": "14:15 - 14:30"
      },
      {
        "id": 74,
        "title": "A Multi-Kernel Convolutional Neural Network Model for Classifying Plant Leaf Diseases",
        "time": "14:30 - 14:45"
      },
      {
        "id": 92,
        "title": "Review paper: Deep Learning Based Biometric Recognition Model Using Finger and Palm Vein Images",
        "time": "14:45 - 15:00"
      },
      {
        "id": 104,
        "title": "Machine Learning-Driven Meta surfaces for Adaptive 6G Beamforming in Dynamic Terahertz Channels",
        "time": "15:00 - 15:15"
      },
      {
        "id": 111,
        "title": "Predicting Adult Income Utilizing Various Artificial Intelligence Models",
        "time": "15:30 - 15:45"
      },
      {
        "id": 114,
        "title": "Analyzing Power Plant Data Using Artificial Intelligence to Enhance Maintenance Strategy ",
        "time": "15:45 - 16:00"
      },
      {
        "id": 193,
        "title": "Leveraging AI for Customer Segmentation and Predictive Insights to Elevate E-Commerce Satisfaction ",
        "time": "16:00 - 16:15"
      },
      {
        "id": 201,
        "title": "PhisNet: Intelligent Detection of Phishing ",
        "time": "16:15 - 16:30"
      },
      {
        "id": 202,
        "title": "A Real-Time Fall Detection Framework using Vision Transformer and LSTM for Elderly People ",
        "time": "16:30 - 16:45"
      }
    ]
  },
  {
    "name": "Technical Session 5: Mechanical Systems, Materials Engineering, and Thermal-Energy Applications",
    "date": "23 July, 2025",
    "time": "14:00 - 16:45",
    "qrdata": "https://events.teams.microsoft.com/event/b72a7877-bbd1-4623-8fca-181f5496a75f@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 82,
        "title": "PMMA/PEEKs/MFP Ternary Composites Mechanical /Morphological Assessment for dental application.",
        "time": "14:00 - 14:15"
      },
      {
        "id": 18,
        "title": "Surface Modification of Mg Alloys for Biomedical Applications Through the Electrospinning Process: A Review ",
        "time": "14:15 - 14:30"
      },
      {
        "id": 105,
        "title": "Insights into Experimental and Numerical Evaluation of Liquid Desiccant Dehumidifier System Powered by Solar System",
        "time": "14:30 - 14:45"
      },
      {
        "id": 80,
        "title": "Investigation of the Effect of Layer Number and Plate Perforation on the Ballistic Performance of Armor: A Review",
        "time": "14:45 - 15:00"
      },
      {
        "id": 70,
        "title": "Numerical Investigation of Thermal - Hydraulic Performance of a Solar Air Heater Duct with transverse W-Shaped Rib Turbulators",
        "time": "15:00 - 15:30"
      },
      {
        "id": 31,
        "title": "Design and analysis of a planetary geared five-bar slider mechanism for generating long dwell periods",
        "time": "15:30 - 15:45"
      },
      {
        "id": 36,
        "title": "Study of 3D-Printed Honeycomb Orientation on Vibration Energy Harvesting",
        "time": "15:45 - 16:00"
      },
      {
        "id": 178,
        "title": "Numerical analysis of perforation steel plates impacted by blunt, conical, hemispherical, and spherical projectiles",
        "time": "16:00 - 16:15"
      },
      {
        "id": 203,
        "title": "Evaluation of Mechanical and Thermal Properties of a Reinforced Thermosetting Polymer with Glass Fiber and Multi-Walled Carbon Nanotubes",
        "time": "16:15 - 16:30"
      },
      {
        "id": 216,
        "title": "Prosthetic Finger Design for Partial Hand Amputees: A Five-Bar Linkage Approach",
        "time": "16:30 - 16:45"
      }
    ]
  },
  {
    "name": "Technical Session 6: Smart and Sustainable Materials in Civil Infrastructure Engineering",
    "date": "23 July, 2025",
    "time": "14:00 - 16:15",
    "qrdata": "https://events.teams.microsoft.com/event/3e1caa67-acd5-4c3b-8827-2270d60f28b6@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 137,
        "title": "The aesthetics of techniques in contemporary interior design  (Kingdom of Jordan News Channel studio as a case study)",
        "time": "14:00 - 14:15"
      },
      {
        "id": 147,
        "title": "An analysis of the environmental impacts of electronic waste and important precautions  ",
        "time": "14:15 - 14:30"
      },
      {
        "id": 190,
        "title": "Reactive Powder Concrete Reinforced with Manufactured Fibers or Recycled from Waste Tire ",
        "time": "14:30 - 14:45"
      },
      {
        "id": 212,
        "title": "Behaviour of Fibre-Reinforced Lightweight Self-Compacting Concrete Containing Recycled Brick Aggregate and Silica Fume ",
        "time": "14:45 - 15:00"
      },
      {
        "id": 192,
        "title": "Valorization of Dredged Sediments from Cameron Highlands Reservoirs: Characterization and Pollution Risk Assessment for Sustainable Construction Materials Recovery  ",
        "time": "15:00 - 15:15"
      },
      {
        "id": 96,
        "title": "Experimental Investigation of Energy Performance in Double-Glazed Windows Utilizing Air and Phase Change Materials",
        "time": "15:30 - 15:45"
      },
      {
        "id": 165,
        "title": "A State-of-the-Art Review of Glazed Fenestration Systems for Enhanced Thermal Performance and Solar Heat Gain Mitigation in Building Envelopes ",
        "time": "15:45 - 16:00"
      },
      {
        "id": 169,
        "title": "Enhancement of wall insulation and reduction of heat gain in buildings by different ways: review",
        "time": "16:00 - 16:15"
      }
    ]
  },
  {
    "name": "Technical Session 7: Hydraulic and Urban Systems in Civil Engineering",
    "date": "23 July, 2025",
    "time": "14:00 - 16:30",
    "qrdata": "https://events.teams.microsoft.com/event/c5894af4-999b-4977-a756-c0b75563dc41@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 57,
        "title": "Structural Performance of High Strength Self-Compaction Concrete Beam with Perforated Steel Box Shear Connectors",
        "time": "14:00 - 14:15"
      },
      {
        "id": 131,
        "title": "Hydrodynamic Based Model to Simulate Water Quality in Kufa River, Iraq",
        "time": "14:15 - 14:30"
      },
      {
        "id": 133,
        "title": "Long Term Degradation of Tigris River at Al-Nuhairat Bridge Location ",
        "time": "14:30 - 14:45"
      },
      {
        "id": 135,
        "title": "Experimental and numerical study of eco-friendly corbels under static loadin",
        "time": "14:45 - 15:00"
      },
      {
        "id": 148,
        "title": "Lead Removal from Water Using CTAB-Enhanced Nanosilica-Coated Sand Barrier under Continuous Flow: Experimental Study and Breakthrough Curve Modelling ",
        "time": "15:00 - 15:15"
      },
      {
        "id": 149,
        "title": "Spatial analysis of noise pollution in the College of Engineering/ University of Basrah using (GIS) technology",
        "time": "15:30 - 15:45"
      },
      {
        "id": 167,
        "title": "Towards Sustainability in Urban Spaces: Evaluating Applied Architectural Ideas",
        "time": "15:45 - 16:00"
      },
      {
        "id": 176,
        "title": "Development of a Curve Number Map for the Ali Al-Gharbi District, Southern Iraq, Using GIS ",
        "time": "16:00 - 16:15"
      },
      {
        "id": 181,
        "title": "Future Forecasts Of Rainfall Utilising The LARS-WG And CMIP6 Models ",
        "time": "16:15 - 16:30"
      }
    ]
  },
  {
    "name": "Technical Session 8: Sustainable Structural Systems and Materials in Civil Engineering",
    "date": "24 July, 2025",
    "time": "10:00 - 12:30",
    "qrdata": "https://events.teams.microsoft.com/event/3f2c9e17-c6a0-4288-a6bd-bb3fecc50f3d@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 55,
        "title": "Structural Behavior of One-Way Reinforced SCC Slabs Made with a Variety of Recycled Aggregates under Repeated Load",
        "time": "10:00 - 10:15"
      },
      {
        "id": 61,
        "title": "Mechanical Properties of Modified Porous Concrete ncorporating Different Types of Lightweight Aggregate ",
        "time": "10:15 - 10:30"
      },
      {
        "id": 46,
        "title": "Flexural Behavior of Hybrid Concrete Tee Beams Reinforced with GFRP Bars",
        "time": "10:30 - 10:45"
      },
      {
        "id": 49,
        "title": "Investigation the Efficacy of Steel Section Reinforcement in Hybrid Deep Beam Applications",
        "time": "10:45 - 11:00"
      },
      {
        "id": 11,
        "title": "Enhancing Metakaolin Reactivity in Geopolymers: A Comprehensive Review of Key Influencing Parameters",
        "time": "11:00 - 11:30"
      },
      {
        "id": 138,
        "title": "Behavior of Recycled Aggregate Concrete Slab\u2013Column Connection Strengthened by NSM GFRP bars ",
        "time": "11:30 - 11:45"
      },
      {
        "id": 183,
        "title": "Influence of steel plate on enhancing the punching strength of voided slabs ",
        "time": "11:45 - 12:00"
      },
      {
        "id": 195,
        "title": "Criteria for Evaluating the Performance of Government Projects ",
        "time": "12:00 - 12:15"
      },
      {
        "id": 210,
        "title": "Development of Sustainable Fibre Reinforced High Strength Lightweight Concrete with Recycled Fine Aggregate and Silica Fume",
        "time": "12:15 - 12:30"
      }
    ]
  },
  {
    "name": "Technical Session 9: Biofuels, Catalysis, and Resource Recovery",
    "date": "24 July, 2025",
    "time": "10:00 - 12:45",
    "qrdata": "https://events.teams.microsoft.com/event/5e396332-5dd3-41c0-993d-78d8c258c6c1@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 15,
        "title": "Pyrolysis of Local Oil Seed for Biodiesel Production: A Review",
        "time": "10:00 - 10:15"
      },
      {
        "id": 44,
        "title": "Catalytic Deoxygenation of Hydrolyzed Animal Fat-Derived Oil Using a Zeolite Catalyst",
        "time": "10:15 - 10:30"
      },
      {
        "id": 66,
        "title": "Enhancing Sulphur Removal from Iraqi Qayyarah Crude Oil through Glass Waste-Based Adsorption at Varied Temperatures and Contact Durations",
        "time": "10:30 - 10:45"
      },
      {
        "id": 77,
        "title": "Optimization of Thermal and Temporal Parameters in Ethanol-Assisted Soxhlet Extraction of Bioactive Drugs: A Kinetic Comparison of Eugenol and Caffeine",
        "time": "10:45 - 11:00"
      },
      {
        "id": 89,
        "title": "Experimental Investigation and optimization for desulfurization of diesel fuel using microwave irradiation and activated carbon ",
        "time": "11:00 - 11:15"
      },
      {
        "id": 94,
        "title": "Catalytic Deoxygenation of Hydrolyzed Oil of Beef Tallow over Lanthanum-Embedded HZSM-5 Zeolite Catalyst to Produce Biofuels",
        "time": "11:30 - 11:45"
      },
      {
        "id": 157,
        "title": "Synthesis and Characterization of Niobium promoted Ni/Mesoporous MCM-41 for potential application in steam reforming of glycerol using a fixed bed reactor ",
        "time": "11:45 - 12:00"
      },
      {
        "id": 164,
        "title": "Elucidating CO2 adsorptivity of Ni-Co-Y/MCM-41 as a potential pathway for CO2 reforming of ethanol ",
        "time": "12:00 - 12:15"
      },
      {
        "id": 189,
        "title": "Screening of hydrophilic deep eutectic solvents for ultrasound probe-assisted extraction of rosmarinic acid from salvia officinalis with high-performance liquid chromatography analysis ",
        "time": "12:15 - 12:30"
      },
      {
        "id": 198,
        "title": "Efficient Glycerol Removal from Biodiesel Using Deep Eutectic Solvents Combined with Activated Carbon ",
        "time": "12:30 - 12:45"
      }
    ]
  },
  {
    "name": "Technical Session 10: Environmental and Wastewater Treatment Technologies",
    "date": "24 July, 2025",
    "time": "10:00 - 12:30",
    "qrdata": "https://events.teams.microsoft.com/event/0e50d0ff-f85b-4d06-9385-bcb8b85ec50f@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 13,
        "title": "Treatment of petroleum refinery wastewater by advance d oxidation process (AOPs) Minireview",
        "time": "10:00 - 10:15"
      },
      {
        "id": 19,
        "title": "Treatment of Petroleum refinery wastewater by electrooxidation using anode composed of composite materials ",
        "time": "10:15 - 10:30"
      },
      {
        "id": 23,
        "title": "Assessment of Photocatalytic Process using composite photocatalysts for COD reduction for Al-Dewaniyah Petroleum refinery wastewater: RSM ",
        "time": "10:30 - 10:45"
      },
      {
        "id": 38,
        "title": "Hydrodynamic Characteristics of Two-Phase Systems in Tapered Bubble Columns (TBCs)",
        "time": "10:45 - 11:00"
      },
      {
        "id": 73,
        "title": "Equilibrium Analysis and Adsorptive Removal of Lead (Pb) by Activated Carbon Derived from Ceratophyllum demersum: Effect of Activation Methods",
        "time": "11:00 - 11:15"
      },
      {
        "id": 97,
        "title": "Adsorptive desulphurization of model diesel by activated carbon loaded with Ni oxide nanoparticles prepared from local Iraqi pomegranate",
        "time": "11:30 - 11:45"
      },
      {
        "id": 115,
        "title": "Modeling of the adsorption process of the organic pollutant from synthetic wastewater using different adsorbents   ",
        "time": "11:45 - 12:00"
      },
      {
        "id": 129,
        "title": "A Review of Natural Clay Ceramic Membranes: Manufacturing Techniques and Implementations in Industrial and Municipal Wastewater Treatment",
        "time": "12:00 - 12:15"
      },
      {
        "id": 143,
        "title": "Kinetic model of Lead (Pb) Adsorption by Raw and Carbonized Ceratophyllum demersum: Mechanisms and Rate Analysis\"\u00a0",
        "time": "12:15 - 12:30"
      }
    ]
  },
  {
    "name": "Technical Session 11: Mechatronics, Robotics, and Smart Automation Systems",
    "date": "24 July, 2025",
    "time": "10:00 - 11:30",
    "qrdata": "https://events.teams.microsoft.com/event/555b314b-2ce8-4107-8b33-2cf3333e0bf8@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 93,
        "title": "Evaluation and Enhancement of Solar Energy-Enabled Intelligent Structural Systems",
        "time": "10:00 - 10:15"
      },
      {
        "id": 87,
        "title": "Investigation of IMU Motion Effects based on MPU 6050 Using a Dynamic Motion Testing Device",
        "time": "10:15 - 10:30"
      },
      {
        "id": 64,
        "title": "Designing a Robotic System for Efficient Exam Paper Distribution Using Multi-Sensor Technology",
        "time": "10:30 - 10:45"
      },
      {
        "id": 52,
        "title": "AI-Based Control of Brushless DC Motors: A Practical Approach to Performance Enhancement",
        "time": "10:45 - 11:00"
      },
      {
        "id": 28,
        "title": "A Novel Coupled-Inductor Boost Converter with ANN Control for High Step-Up PV Systems",
        "time": "11:00 - 11:15"
      },
      {
        "id": 174,
        "title": "Artificial Neural Network-Based Control of Vienna Rectifier for Power Factor Correction and Capacitor Voltage Balancing ",
        "time": "11:15 - 11:30"
      }
    ]
  },
  {
    "name": "Technical Session 12: Smart Computing, IoT Systems, and Intelligent Infrastructure",
    "date": "24 July, 2025",
    "time": "10:00 - 12:45",
    "qrdata": "https://events.teams.microsoft.com/event/656ac187-60be-4a74-9f47-03a0e7374ebf@051008eb-db40-4249-9ece-9df3e8c3f594",
    "papers": [
      {
        "id": 35,
        "title": "Evolutionary Algorithms for Iot Service Select\u0131on: A Review",
        "time": "10:00 - 10:15"
      },
      {
        "id": 48,
        "title": "Intelligent Control for Video Broadcasting in Flying Ad Hoc Networks: A Simulation Study",
        "time": "10:15 - 10:30"
      },
      {
        "id": 90,
        "title": "Patient-Specific 3D-Printed Cutting and Repositioning Guide for Mandibular Tumor Resection: Surgical Design and Validation",
        "time": "10:30 - 10:45"
      },
      {
        "id": 113,
        "title": "Swarm Intelligence in Modern Engineering    A Comprehensive Review of Applications, Performance, and Emerging Trends    ",
        "time": "10:45 - 11:00"
      },
      {
        "id": 136,
        "title": "Learning About Syndrome Awareness and WMS Algorithm for Adaptive Neural Decoding for 6G LDPC Base Graph Enhancement",
        "time": "11:00 - 11:15"
      },
      {
        "id": 153,
        "title": "Design and Implementation of a Low Cost IoT-Based System for Enhanced Visual Feedback, Alert Systems, and Server Environment Tracking ",
        "time": "11:30 - 11:45"
      },
      {
        "id": 194,
        "title": "Leveraging Augmented and Virtual Reality for Enhancing Eco-Literacy: A Study on Sustainable Green Education Using Immersive Technologies ",
        "time": "11:45 - 12:00"
      },
      {
        "id": 197,
        "title": "Automated Greenhouse Management System with IOT Integration ",
        "time": "12:00 - 12:15"
      },
      {
        "id": 199,
        "title": "Developing a program to track the performance of multiple projects using Earned Value and Scorecard technology ",
        "time": "12:15 - 12:30"
      },
      {
        "id": 14,
        "title": "Design and Implementation of an IoT-Based System for Remote Monitoring of Vital Signs",
        "time": "12:30 - 12:45"
      }
    ]
  }
])
</script>

<template>
  <Main></Main>
  <div class="flex justify-center">
  <Card pt:content:class="flex flex-col gap-3" pt:root:class="max-w-4xl">
    <template #title><span class="font-light">Technical Sessions</span></template>
    <template #content>
      <Panel toggleable collapsed header="How to join a technical session?" pt:header:class="!bg-primary-300">
        <div class="mt-2 pl-5">
          <ol class="list-decimal">
            <li>
              Scan the QR code or click on the <Button>Event Page</Button> under the relevant Technical Session to go to its respective event page.
            </li>
            <li>
              On the event page, click the <Button class="teamsbutton">Register</Button> to go the registration page.
              <br>
              <div class="instructionimagecontainer"><img class="instructionimage" :src="ImgRegister"/></div>
            </li>
            <li>
              Fill in your name, email address, and agree to the terms and conditions before clicking the  <Button class="teamsbutton">Register</Button>.
              <br>
              <img class="instructionimage" :src="ImgParticipants"/>
            </li>
            <li>
              You will see a dialog box indicating successful registration.
              <br>
              <img class="instructionimage" :src="ImgConfirmation"/>
            </li>
          </ol>
        </div>
      </Panel>
      <Accordion value="0">
        <AccordionPanel v-for="(session, index) in sessions" :key="index" :value="index">
          <AccordionHeader>
            <div>
              <div>{{ session.name }}</div>
              <div class="font-thin text-sm">{{ session.date }} ({{ session.time }})</div>
            </div></AccordionHeader>
          <AccordionContent pt:content:class="flex flex-col md:flex-row items-center justify-center md:items-start md:justify-center">
            <div class="flex flex-col justify-center items-center shrink-0" v-if="session.qrdata">
              <Qrcode :value="session.qrdata" :size="200" :margin="2" class="w-full max-w-50"></Qrcode>
              <a :href="session.qrdata" target="_blank"><Button>Event Page</Button></a>
            </div>
            <div class="flex flex-col gap-3 w-full">
              <div v-for="paper in session.papers" :key="paper.id">
                <Card>
                  <template #title>Paper ID: {{ paper.id }}</template>
                  <template #subtitle>{{ paper.time }}</template>
                  <template #content>{{ paper.title }}</template>
                </Card>
              </div>
            </div>
          </AccordionContent>
        </AccordionPanel>
      </Accordion>
    </template>
  </Card>
  </div>
</template>

<style scoped>
@reference "../src/style.css";
.teamsbutton {
  background-color: #5B5FC7;
  color: white;
  border-color: #5B5FC7;
}

.teamsbutton:hover {
  background-color: #4F52B2;
  color: white;
  border-color: #4F52B2;
}

.instructionimagecontainer {
  @apply w-full text-center
}
.instructionimage {
  @apply border border-primary my-2 p-2 border-2 max-w-8/10
}
</style>