import 'package:flutter/material.dart';

void main() {
  runApp(const HospitalApp());
}

class HospitalApp extends StatelessWidget {
  const HospitalApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'MediCare Hospital',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(
          seedColor: Colors.blue,
        ),
        useMaterial3: true,
      ),
      home: const LoginPage(),
    );
  }
}

// ======================================================
// LOGIN PAGE
// ======================================================

class LoginPage extends StatelessWidget {
  const LoginPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.blue.shade50,
      body: Center(
        child: SingleChildScrollView(
          padding: const EdgeInsets.all(20),
          child: Container(
            width: 500,
            padding: const EdgeInsets.all(30),
            decoration: BoxDecoration(
              color: Colors.white,
              borderRadius: BorderRadius.circular(10),
              boxShadow: [
                BoxShadow(
                  color: Colors.black.withOpacity(0.08),
                  blurRadius: 15,
                ),
              ],
            ),
            child: Column(
              mainAxisSize: MainAxisSize.min,
              children: [

                const Icon(
                  Icons.local_hospital,
                  size: 60,
                  color: Colors.blue,
                ),

                const SizedBox(height: 15),

                const Text(
                  "MediCare Hospital",
                  style: TextStyle(
                    fontSize: 26,
                    fontWeight: FontWeight.bold,
                    color: Colors.blue,
                  ),
                ),

                const SizedBox(height: 5),

                const Text(
                  "Login to continue",
                  style: TextStyle(
                    color: Colors.grey,
                    fontSize: 15,
                  ),
                ),

                const SizedBox(height: 30),

                TextField(
                  decoration: InputDecoration(
                    labelText: "Email",
                    prefixIcon: const Icon(
                      Icons.email_outlined,
                    ),
                    border: OutlineInputBorder(
                      borderRadius:
                          BorderRadius.circular(6),
                    ),
                  ),
                ),

                const SizedBox(height: 20),

                TextField(
                  obscureText: true,
                  decoration: InputDecoration(
                    labelText: "Password",
                    prefixIcon: const Icon(
                      Icons.lock_outline,
                    ),
                    border: OutlineInputBorder(
                      borderRadius:
                          BorderRadius.circular(6),
                    ),
                  ),
                ),

                const SizedBox(height: 25),

                SizedBox(
                  width: double.infinity,
                  height: 50,
                  child: ElevatedButton(
                    onPressed: () {

                      // OPEN HOSPITAL HOME PAGE
                      Navigator.pushReplacement(
                        context,
                        MaterialPageRoute(
                          builder: (context) =>
                              const HospitalHomePage(),
                        ),
                      );
                    },
                    style: ElevatedButton.styleFrom(
                      backgroundColor: Colors.blue,
                      foregroundColor: Colors.white,
                    ),
                    child: const Text(
                      "LOGIN",
                      style: TextStyle(
                        fontSize: 18,
                      ),
                    ),
                  ),
                ),

                const SizedBox(height: 10),

                TextButton(
                  onPressed: () {},
                  child: const Text(
                    "Forgot Password?",
                  ),
                ),
              ],
            ),
          ),
        ),
      ),
    );
  }
}

// ======================================================
// HOSPITAL HOME PAGE
// ======================================================

class HospitalHomePage extends StatelessWidget {
  const HospitalHomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text(
          "MediCare Hospital",
          style: TextStyle(
            fontWeight: FontWeight.bold,
          ),
        ),
        backgroundColor: Colors.blue,
        foregroundColor: Colors.white,

        actions: [
          IconButton(
            onPressed: () {},
            icon: const Icon(
              Icons.notifications,
            ),
          ),
        ],
      ),

      body: SingleChildScrollView(
        padding: const EdgeInsets.all(16),

        child: Column(
          crossAxisAlignment:
              CrossAxisAlignment.start,
          children: [

            const Text(
              "Welcome 👋",
              style: TextStyle(
                fontSize: 26,
                fontWeight: FontWeight.bold,
              ),
            ),

            const SizedBox(height: 5),

            const Text(
              "How can we help you today?",
              style: TextStyle(
                color: Colors.grey,
                fontSize: 16,
              ),
            ),

            const SizedBox(height: 20),

            // SEARCH
            TextField(
              decoration: InputDecoration(
                hintText:
                    "Search doctors or departments",
                prefixIcon:
                    const Icon(Icons.search),
                border: OutlineInputBorder(
                  borderRadius:
                      BorderRadius.circular(15),
                ),
              ),
            ),

            const SizedBox(height: 20),

            // EMERGENCY
            Container(
              width: double.infinity,
              padding: const EdgeInsets.all(20),
              decoration: BoxDecoration(
                color: Colors.red,
                borderRadius:
                    BorderRadius.circular(18),
              ),

              child: const Column(
                crossAxisAlignment:
                    CrossAxisAlignment.start,
                children: [

                  Icon(
                    Icons.emergency,
                    color: Colors.white,
                    size: 40,
                  ),

                  SizedBox(height: 10),

                  Text(
                    "Emergency Services",
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 21,
                      fontWeight: FontWeight.bold,
                    ),
                  ),

                  SizedBox(height: 5),

                  Text(
                    "Emergency Number: 108",
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 16,
                    ),
                  ),
                ],
              ),
            ),

            const SizedBox(height: 25),

            const Text(
              "Quick Services",
              style: TextStyle(
                fontSize: 21,
                fontWeight: FontWeight.bold,
              ),
            ),

            const SizedBox(height: 15),

            // QUICK SERVICES
            Row(
              children: [

                Expanded(
                  child: _serviceButton(
                    context,
                    Icons.calendar_month,
                    "Appointment",
                    Colors.blue,
                    const AppointmentPage(),
                  ),
                ),

                const SizedBox(width: 10),

                Expanded(
                  child: _serviceButton(
                    context,
                    Icons.people,
                    "Doctors",
                    Colors.green,
                    const DoctorsPage(),
                  ),
                ),

                const SizedBox(width: 10),

                Expanded(
                  child: _serviceButton(
                    context,
                    Icons.local_hospital,
                    "Departments",
                    Colors.orange,
                    const DepartmentsPage(),
                  ),
                ),
              ],
            ),

            const SizedBox(height: 25),

            const Text(
              "Hospital Information",
              style: TextStyle(
                fontSize: 21,
                fontWeight: FontWeight.bold,
              ),
            ),

            const SizedBox(height: 15),

            _infoCard(
              Icons.info_outline,
              "About Hospital",
              "Modern healthcare facilities and experienced doctors.",
            ),

            _infoCard(
              Icons.access_time,
              "Opening Hours",
              "Hospital services available 24 hours.",
            ),

            _infoCard(
              Icons.medical_services,
              "Facilities",
              "ICU, Pharmacy, Laboratory, Radiology and more.",
            ),

            const SizedBox(height: 25),

            // CONTACT
            Container(
              width: double.infinity,
              padding: const EdgeInsets.all(20),
              decoration: BoxDecoration(
                color: Colors.blue,
                borderRadius:
                    BorderRadius.circular(18),
              ),

              child: Column(
                crossAxisAlignment:
                    CrossAxisAlignment.start,
                children: [

                  const Text(
                    "Need Help?",
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 21,
                      fontWeight: FontWeight.bold,
                    ),
                  ),

                  const SizedBox(height: 8),

                  const Text(
                    "Contact our hospital team.",
                    style: TextStyle(
                      color: Colors.white70,
                    ),
                  ),

                  const SizedBox(height: 15),

                  ElevatedButton(
                    onPressed: () {
                      Navigator.push(
                        context,
                        MaterialPageRoute(
                          builder: (context) =>
                              const ContactPage(),
                        ),
                      );
                    },
                    child: const Text(
                      "View Contact Numbers",
                    ),
                  ),
                ],
              ),
            ),

            const SizedBox(height: 30),
          ],
        ),
      ),

      // BOTTOM NAVIGATION
      bottomNavigationBar:
          BottomNavigationBar(
        currentIndex: 0,
        selectedItemColor: Colors.blue,

        onTap: (index) {

          if (index == 1) {
            Navigator.push(
              context,
              MaterialPageRoute(
                builder: (context) =>
                    const AppointmentPage(),
              ),
            );
          }

          if (index == 2) {
            Navigator.push(
              context,
              MaterialPageRoute(
                builder: (context) =>
                    const DoctorsPage(),
              ),
            );
          }
        },

        items: const [

          BottomNavigationBarItem(
            icon: Icon(Icons.home),
            label: "Home",
          ),

          BottomNavigationBarItem(
            icon: Icon(Icons.calendar_month),
            label: "Appointments",
          ),

          BottomNavigationBarItem(
            icon: Icon(Icons.people),
            label: "Doctors",
          ),
        ],
      ),
    );
  }

  Widget _serviceButton(
    BuildContext context,
    IconData icon,
    String title,
    Color color,
    Widget page,
  ) {
    return InkWell(
      onTap: () {
        Navigator.push(
          context,
          MaterialPageRoute(
            builder: (context) => page,
          ),
        );
      },

      child: Container(
        height: 110,

        decoration: BoxDecoration(
          color: color.withOpacity(0.1),
          borderRadius:
              BorderRadius.circular(15),
        ),

        child: Column(
          mainAxisAlignment:
              MainAxisAlignment.center,

          children: [

            Icon(
              icon,
              color: color,
              size: 35,
            ),

            const SizedBox(height: 8),

            Text(
              title,
              textAlign: TextAlign.center,
              style: const TextStyle(
                fontWeight: FontWeight.bold,
              ),
            ),
          ],
        ),
      ),
    );
  }

  Widget _infoCard(
    IconData icon,
    String title,
    String description,
  ) {
    return Card(
      margin:
          const EdgeInsets.only(bottom: 12),

      child: ListTile(

        leading: CircleAvatar(
          backgroundColor:
              Colors.blue.withOpacity(0.1),

          child: Icon(
            icon,
            color: Colors.blue,
          ),
        ),

        title: Text(
          title,
          style: const TextStyle(
            fontWeight: FontWeight.bold,
          ),
        ),

        subtitle: Text(description),
      ),
    );
  }
}

// ======================================================
// APPOINTMENT PAGE
// ======================================================

class AppointmentPage extends StatefulWidget {
  const AppointmentPage({super.key});

  @override
  State<AppointmentPage> createState() =>
      _AppointmentPageState();
}

class _AppointmentPageState
    extends State<AppointmentPage> {

  final formKey =
      GlobalKey<FormState>();

  String gender = "Male";
  String department = "Cardiology";
  String doctor = "Dr. Raj Kumar";

  DateTime? appointmentDate;
  TimeOfDay? appointmentTime;

  Future<void> chooseDate() async {

    final date =
        await showDatePicker(
      context: context,
      initialDate: DateTime.now(),
      firstDate: DateTime.now(),
      lastDate: DateTime(2030),
    );

    if (date != null) {
      setState(() {
        appointmentDate = date;
      });
    }
  }

  Future<void> chooseTime() async {

    final time =
        await showTimePicker(
      context: context,
      initialTime: TimeOfDay.now(),
    );

    if (time != null) {
      setState(() {
        appointmentTime = time;
      });
    }
  }

  void submitAppointment() {

    if (!formKey.currentState!.validate()) {
      return;
    }

    if (appointmentDate == null ||
        appointmentTime == null) {

      ScaffoldMessenger.of(context)
          .showSnackBar(
        const SnackBar(
          content: Text(
            "Please select date and time.",
          ),
        ),
      );

      return;
    }

    showDialog(
      context: context,

      builder: (context) {
        return AlertDialog(
          title: const Text(
            "Appointment Submitted",
          ),

          content: const Text(
            "Your appointment request has been submitted successfully.",
          ),

          actions: [
            TextButton(
              onPressed: () {
                Navigator.pop(context);
              },
              child: const Text("OK"),
            ),
          ],
        );
      },
    );
  }

  @override
  Widget build(BuildContext context) {

    return Scaffold(
      appBar: AppBar(
        title: const Text(
          "Book Appointment",
        ),
        backgroundColor: Colors.blue,
        foregroundColor: Colors.white,
      ),

      body: SingleChildScrollView(
        padding: const EdgeInsets.all(20),

        child: Form(
          key: formKey,

          child: Column(
            crossAxisAlignment:
                CrossAxisAlignment.start,
            children: [

              const Text(
                "Patient Details",
                style: TextStyle(
                  fontSize: 22,
                  fontWeight: FontWeight.bold,
                ),
              ),

              const SizedBox(height: 20),

              TextFormField(
                decoration:
                    const InputDecoration(
                  labelText: "Patient Name",
                  prefixIcon:
                      Icon(Icons.person),
                  border:
                      OutlineInputBorder(),
                ),

                validator: (value) {
                  if (value == null ||
                      value.trim().isEmpty) {
                    return "Enter patient name";
                  }
                  return null;
                },
              ),

              const SizedBox(height: 15),

              TextFormField(
                keyboardType:
                    TextInputType.number,

                decoration:
                    const InputDecoration(
                  labelText: "Age",
                  prefixIcon:
                      Icon(Icons.cake),
                  border:
                      OutlineInputBorder(),
                ),

                validator: (value) {
                  if (value == null ||
                      value.trim().isEmpty) {
                    return "Enter age";
                  }
                  return null;
                },
              ),

              const SizedBox(height: 15),

              DropdownButtonFormField<String>(
                value: gender,

                decoration:
                    const InputDecoration(
                  labelText: "Gender",
                  prefixIcon:
                      Icon(Icons.people),
                  border:
                      OutlineInputBorder(),
                ),

                items: const [

                  DropdownMenuItem(
                    value: "Male",
                    child: Text("Male"),
                  ),

                  DropdownMenuItem(
                    value: "Female",
                    child: Text("Female"),
                  ),

                  DropdownMenuItem(
                    value: "Other",
                    child: Text("Other"),
                  ),
                ],

                onChanged: (value) {
                  setState(() {
                    gender = value!;
                  });
                },
              ),

              const SizedBox(height: 15),

              TextFormField(
                keyboardType:
                    TextInputType.phone,

                decoration:
                    const InputDecoration(
                  labelText: "Phone Number",
                  prefixIcon:
                      Icon(Icons.phone),
                  border:
                      OutlineInputBorder(),
                ),

                validator: (value) {
                  if (value == null ||
                      value.length < 10) {
                    return "Enter valid phone number";
                  }
                  return null;
                },
              ),

              const SizedBox(height: 25),

              const Text(
                "Appointment Details",
                style: TextStyle(
                  fontSize: 22,
                  fontWeight: FontWeight.bold,
                ),
              ),

              const SizedBox(height: 20),

              DropdownButtonFormField<String>(
                value: department,

                decoration:
                    const InputDecoration(
                  labelText: "Department",
                  prefixIcon:
                      Icon(Icons.local_hospital),
                  border:
                      OutlineInputBorder(),
                ),

                items: const [

                  DropdownMenuItem(
                    value: "Cardiology",
                    child: Text("Cardiology"),
                  ),

                  DropdownMenuItem(
                    value: "Neurology",
                    child: Text("Neurology"),
                  ),

                  DropdownMenuItem(
                    value: "Pediatrics",
                    child: Text("Pediatrics"),
                  ),

                  DropdownMenuItem(
                    value: "Orthopedics",
                    child: Text("Orthopedics"),
                  ),

                  DropdownMenuItem(
                    value: "General Medicine",
                    child: Text("General Medicine"),
                  ),
                ],

                onChanged: (value) {
                  setState(() {
                    department = value!;
                  });
                },
              ),

              const SizedBox(height: 15),

              DropdownButtonFormField<String>(
                value: doctor,

                decoration:
                    const InputDecoration(
                  labelText: "Doctor",
                  prefixIcon:
                      Icon(Icons.person),
                  border:
                      OutlineInputBorder(),
                ),

                items: const [

                  DropdownMenuItem(
                    value: "Dr. Raj Kumar",
                    child:
                        Text("Dr. Raj Kumar"),
                  ),

                  DropdownMenuItem(
                    value: "Dr. Priya Sharma",
                    child:
                        Text("Dr. Priya Sharma"),
                  ),

                  DropdownMenuItem(
                    value: "Dr. Anil Reddy",
                    child:
                        Text("Dr. Anil Reddy"),
                  ),
                ],

                onChanged: (value) {
                  setState(() {
                    doctor = value!;
                  });
                },
              ),

              const SizedBox(height: 15),

              SizedBox(
                width: double.infinity,
                height: 50,

                child: OutlinedButton.icon(
                  onPressed: chooseDate,

                  icon: const Icon(
                    Icons.calendar_month,
                  ),

                  label: Text(
                    appointmentDate == null
                        ? "Select Date"
                        : "${appointmentDate!.day}/"
                          "${appointmentDate!.month}/"
                          "${appointmentDate!.year}",
                  ),
                ),
              ),

              const SizedBox(height: 15),

              SizedBox(
                width: double.infinity,
                height: 50,

                child: OutlinedButton.icon(
                  onPressed: chooseTime,

                  icon: const Icon(
                    Icons.access_time,
                  ),

                  label: Text(
                    appointmentTime == null
                        ? "Select Time"
                        : appointmentTime!
                            .format(context),
                  ),
                ),
              ),

              const SizedBox(height: 15),

              TextFormField(
                maxLines: 4,

                decoration:
                    const InputDecoration(
                  labelText:
                      "Health Problem / Reason",
                  alignLabelWithHint: true,
                  prefixIcon:
                      Icon(Icons.notes),
                  border:
                      OutlineInputBorder(),
                ),
              ),

              const SizedBox(height: 30),

              SizedBox(
                width: double.infinity,
                height: 55,

                child: ElevatedButton(
                  onPressed:
                      submitAppointment,

                  style:
                      ElevatedButton.styleFrom(
                    backgroundColor:
                        Colors.blue,
                    foregroundColor:
                        Colors.white,
                  ),

                  child: const Text(
                    "BOOK APPOINTMENT",
                    style: TextStyle(
                      fontSize: 16,
                      fontWeight:
                          FontWeight.bold,
                    ),
                  ),
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}

// ======================================================
// CONTACT PAGE
// ======================================================

class ContactPage extends StatelessWidget {
  const ContactPage({super.key});

  @override
  Widget build(BuildContext context) {

    return Scaffold(
      appBar: AppBar(
        title:
            const Text("Contact Hospital"),
        backgroundColor: Colors.blue,
        foregroundColor: Colors.white,
      ),

      body: ListView(
        padding:
            const EdgeInsets.all(20),

        children: [

          const Text(
            "Hospital Contact Numbers",
            style: TextStyle(
              fontSize: 24,
              fontWeight: FontWeight.bold,
            ),
          ),

          const SizedBox(height: 20),

          _contactCard(
            "Emergency",
            "108",
            Icons.emergency,
            Colors.red,
          ),

          _contactCard(
            "Hospital Reception",
            "+91 98765 43210",
            Icons.local_hospital,
            Colors.blue,
          ),

          _contactCard(
            "Appointment Desk",
            "+91 98765 43211",
            Icons.calendar_month,
            Colors.green,
          ),

          _contactCard(
            "Pharmacy",
            "+91 98765 43212",
            Icons.medication,
            Colors.orange,
          ),

          _contactCard(
            "Ambulance",
            "+91 98765 43213",
            Icons.airport_shuttle,
            Colors.purple,
          ),

          const SizedBox(height: 20),

          const Card(
            child: Padding(
              padding:
                  EdgeInsets.all(20),

              child: Column(
                crossAxisAlignment:
                    CrossAxisAlignment.start,

                children: [

                  Text(
                    "Hospital Address",
                    style: TextStyle(
                      fontSize: 18,
                      fontWeight:
                          FontWeight.bold,
                    ),
                  ),

                  SizedBox(height: 8),

                  Text(
                    "MediCare Hospital\n"
                    "Main Road\n"
                    "Andhra Pradesh, India",
                  ),
                ],
              ),
            ),
          ),
        ],
      ),
    );
  }

  Widget _contactCard(
    String title,
    String number,
    IconData icon,
    Color color,
  ) {

    return Card(
      margin:
          const EdgeInsets.only(
        bottom: 15,
      ),

      child: ListTile(

        contentPadding:
            const EdgeInsets.all(12),

        leading: CircleAvatar(
          backgroundColor:
              color.withOpacity(0.15),

          child: Icon(
            icon,
            color: color,
          ),
        ),

        title: Text(
          title,
          style: const TextStyle(
            fontWeight:
                FontWeight.bold,
          ),
        ),

        subtitle: Text(number),

        trailing: Icon(
          Icons.phone,
          color: color,
        ),
      ),
    );
  }
}

// ======================================================
// DOCTORS PAGE
// ======================================================

class DoctorsPage extends StatelessWidget {
  const DoctorsPage({super.key});

  @override
  Widget build(BuildContext context) {

    return Scaffold(
      appBar: AppBar(
        title:
            const Text("Our Doctors"),
        backgroundColor: Colors.blue,
        foregroundColor: Colors.white,
      ),

      body: ListView(
        padding:
            const EdgeInsets.all(16),

        children: const [

          DoctorCard(
            name: "Dr. Raj Kumar",
            department: "Cardiology",
          ),

          DoctorCard(
            name: "Dr. Priya Sharma",
            department: "Neurology",
          ),

          DoctorCard(
            name: "Dr. Anil Reddy",
            department: "Orthopedics",
          ),

          DoctorCard(
            name: "Dr. Sneha Rao",
            department: "Pediatrics",
          ),
        ],
      ),
    );
  }
}

class DoctorCard extends StatelessWidget {

  final String name;
  final String department;

  const DoctorCard({
    super.key,
    required this.name,
    required this.department,
  });

  @override
  Widget build(BuildContext context) {

    return Card(
      margin:
          const EdgeInsets.only(
        bottom: 15,
      ),

      child: ListTile(

        leading:
            const CircleAvatar(
          radius: 28,
          child: Icon(Icons.person),
        ),

        title: Text(
          name,
          style: const TextStyle(
            fontWeight:
                FontWeight.bold,
          ),
        ),

        subtitle:
            Text(department),
      ),
    );
  }
}

// ======================================================
// DEPARTMENTS PAGE
// ======================================================

class DepartmentsPage
    extends StatelessWidget {

  const DepartmentsPage({super.key});

  @override
  Widget build(BuildContext context) {

    final departments = [
      "Cardiology",
      "Neurology",
      "Pediatrics",
      "Orthopedics",
      "General Medicine",
      "Dermatology",
      "ENT",
      "Gynecology",
    ];

    return Scaffold(
      appBar: AppBar(
        title:
            const Text("Departments"),
        backgroundColor: Colors.blue,
        foregroundColor: Colors.white,
      ),

      body: ListView.builder(
        padding:
            const EdgeInsets.all(16),

        itemCount:
            departments.length,

        itemBuilder:
            (context, index) {

          return Card(
            margin:
                const EdgeInsets.only(
              bottom: 10,
            ),

            child: ListTile(

              leading: const Icon(
                Icons.local_hospital,
                color: Colors.blue,
              ),

              title: Text(
                departments[index],
                style:
                    const TextStyle(
                  fontWeight:
                      FontWeight.bold,
                ),
              ),

              trailing:
                  const Icon(
                Icons.arrow_forward_ios,
                size: 16,
              ),
            ),
          );
        },
      ),
    );
  }
}

