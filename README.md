# AP18110010326-CD-LAB

import net.sf.jasperreports.engine.*;
import net.sf.jasperreports.engine.data.JRBeanCollectionDataSource;
import net.sf.jasperreports.engine.export.JRPdfExporter;
import net.sf.jasperreports.export.SimpleExporterInput;
import net.sf.jasperreports.export.SimpleOutputStreamExporterOutput;
import net.sf.jasperreports.export.SimplePdfExporterConfiguration;

import java.math.BigDecimal;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

public class Report {
	public static void main(String[] args) throws JRException {
		try {
			//String filePath = "C:\\Users\\usman\\pp\\src\\resources\\Simple_Blue.jrxml";
			//String filePath1="C:\\Users\\usman\\pp\\src\\resources\\Leaf_Green_1.jrxml";
			String filePath2="C:\\Users\\usman\\pp\\src\\resources\\Blank_A4_2.jrxml";
			Map<String, Object> parameters = new HashMap<>();
			parameters.put("ptr1", "$4551");
			parameters.put("ptr2", "$2342");
			parameters.put("ptr3", "$3443");
			parameters.put("ptr4", "$554");
			parameters.put("ptr5", "$2235");
			parameters.put("act1", "$345");
			parameters.put("act2", "$35");
			parameters.put("act3", "$534");
			parameters.put("act4", "$3532");
			parameters.put("act5", "$5225");
			parameters.put("ccv1", "$45");
			parameters.put("ccv2", "$45");
			parameters.put("ccv3", "$534");
			parameters.put("ccv4", "$32");
			parameters.put("ccv5", "$235");
			parameters.put("nct1", "$405");
			parameters.put("nct2", "$345");
			parameters.put("nct3", "$434");
			parameters.put("nct4", "$542");
			parameters.put("nct5", "$235");
			parameters.put("ts1", "$540");
			parameters.put("ts2", "$35");
			parameters.put("ts3", "$453");
			parameters.put("ts4", "$342");
			parameters.put("ts5", "$235");
			parameters.put("acv1", "$44");
			parameters.put("acv2", "$54");
			parameters.put("acv3", "$4534");
			parameters.put("acv4", "$432");
			parameters.put("acv5", "$535");
			/*List<Student> studentList = new ArrayList();
			Student student = new Student(1, "sd", "sf",
					"ffe", "sff");
			Student student1 = new Student(2, "d", "sf",
					"fe", "sf");
			studentList.add(student);
			studentList.add(student1);
			List<User> userList=new ArrayList<>();
			User user=new User(1,"jsnjs",new BigDecimal(1.2));
			User user1=new User(11,"jsnjs",new BigDecimal(1.1));
			User user2=new User(111,"jsnjs",new BigDecimal(1));
			userList.add(user);userList.add(user1);userList.add(user2);
			JRBeanCollectionDataSource dataSource = new JRBeanCollectionDataSource(studentList);*/
			JREmptyDataSource dataSource2 = new JREmptyDataSource(1);
			//JasperReport report = JasperCompileManager.compileReport(filePath);
			JasperReport report2 = JasperCompileManager.compileReport(filePath2);
			JasperPrint print = JasperFillManager.fillReport(report2, parameters, dataSource2);
			/*JasperPrint print1 = JasperFillManager.fillReport(report1, parameters, dataSource1);
			List<JasperPrint> jasperPrintList = new ArrayList<JasperPrint>();
			jasperPrintList.add(print);jasperPrintList.add(print1);
			JRPdfExporter exporter = new JRPdfExporter();
			exporter.setExporterInput(SimpleExporterInput.getInstance(jasperPrintList)); //Set as export input my list with JasperPrint s
			exporter.setExporterOutput(new SimpleOutputStreamExporterOutput("D:\\pdfreports\\report.pdf")); //or any other out streaam
			SimplePdfExporterConfiguration configuration = new SimplePdfExporterConfiguration();
			configuration.setCreatingBatchModeBookmarks(true); //add this so your bookmarks work, you may set other parameters
			exporter.setConfiguration(configuration);
			exporter.exportReport();*/
			JasperExportManager.exportReportToPdfFile(print, "D:\\pdfreports\\roiTable.pdf");
			System.out.println("report created");
		}
		catch (Exception e){
			System.out.println(e.toString());
		}
	}
}









<?xml version="1.0" encoding="UTF-8"?>
<!-- Created with Jaspersoft Studio version 6.20.0.final using JasperReports Library version 6.20.0-2bc7ab61c56f459e8176eb05c7705e145cd400ad  -->
<jasperReport xmlns="http://jasperreports.sourceforge.net/jasperreports" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports http://jasperreports.sourceforge.net/xsd/jasperreport.xsd" name="Blank_A4_2" pageWidth="595" pageHeight="842" columnWidth="555" leftMargin="20" rightMargin="20" topMargin="20" bottomMargin="20" uuid="df7b386d-ea38-44d8-bcf6-e30d386494f9">
	<property name="com.jaspersoft.studio.data.defaultdataadapter" value="One Empty Record"/>
	<style name="Table 1_TH" mode="Opaque" backcolor="#F0F8FF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 1_CH" mode="Opaque" backcolor="#BFE1FF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 1_TD" mode="Opaque" backcolor="#FFFFFF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 2_TH" mode="Opaque" backcolor="#F0F8FF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 2_CH" mode="Opaque" backcolor="#BFE1FF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 2_TD" mode="Opaque" backcolor="#FFFFFF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 3_TH" mode="Opaque" backcolor="#EB9123">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 3_CH" mode="Opaque" backcolor="#F5F7FA">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 3_TD" mode="Opaque" backcolor="#FFFFFF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 4_TH" mode="Opaque" backcolor="#F0F8FF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 4_CH" mode="Opaque" backcolor="#F2F8FC">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 4_TD" mode="Opaque" backcolor="#FFFFFF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 5_TH" mode="Opaque" backcolor="#FAFDFF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 5_CH" mode="Opaque" backcolor="#FFFFFF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<style name="Table 5_TD" mode="Opaque" backcolor="#FFFFFF">
		<box>
			<pen lineWidth="0.5" lineColor="#000000"/>
			<topPen lineWidth="0.5" lineColor="#000000"/>
			<leftPen lineWidth="0.5" lineColor="#000000"/>
			<bottomPen lineWidth="0.5" lineColor="#000000"/>
			<rightPen lineWidth="0.5" lineColor="#000000"/>
		</box>
	</style>
	<subDataset name="Dataset1" uuid="20d8c482-9227-4a09-8131-63cf197c5015">
		<parameter name="ptr1" class="java.lang.String"/>
		<parameter name="ptr2" class="java.lang.String"/>
		<parameter name="ptr3" class="java.lang.String"/>
		<parameter name="ptr4" class="java.lang.String"/>
		<parameter name="ptr5" class="java.lang.String"/>
		<parameter name="act1" class="java.lang.String"/>
		<parameter name="act2" class="java.lang.String"/>
		<parameter name="act3" class="java.lang.String"/>
		<parameter name="act4" class="java.lang.String"/>
		<parameter name="act5" class="java.lang.String"/>
		<parameter name="acv1" class="java.lang.String"/>
		<parameter name="acv2" class="java.lang.String"/>
		<parameter name="acv3" class="java.lang.String"/>
		<parameter name="acv4" class="java.lang.String"/>
		<parameter name="acv5" class="java.lang.String"/>
		<parameter name="nct1" class="java.lang.String"/>
		<parameter name="nct2" class="java.lang.String"/>
		<parameter name="nct3" class="java.lang.String"/>
		<parameter name="nct4" class="java.lang.String"/>
		<parameter name="nct5" class="java.lang.String"/>
		<parameter name="ccv1" class="java.lang.String"/>
		<parameter name="ccv2" class="java.lang.String"/>
		<parameter name="ccv3" class="java.lang.String"/>
		<parameter name="ccv4" class="java.lang.String"/>
		<parameter name="ccv5" class="java.lang.String"/>
		<parameter name="ts1" class="java.lang.String"/>
		<parameter name="ts2" class="java.lang.String"/>
		<parameter name="ts3" class="java.lang.String"/>
		<parameter name="ts4" class="java.lang.String"/>
		<parameter name="ts5" class="java.lang.String"/>
		<queryString>
			<![CDATA[]]>
		</queryString>
	</subDataset>
	<subDataset name="Dataset2" uuid="7c61ac01-5958-4780-859f-25b836f76d8e">
		<queryString>
			<![CDATA[]]>
		</queryString>
	</subDataset>
	<subDataset name="Dataset3" uuid="6fb37d0a-7ffd-4e12-b74b-78c0a010c7b8">
		<queryString>
			<![CDATA[]]>
		</queryString>
	</subDataset>
	<subDataset name="Dataset4" uuid="84771581-1b56-40b8-8903-6bc3cf30159d">
		<parameter name="ptr1" class="java.lang.String"/>
		<parameter name="ptr2" class="java.lang.String"/>
		<parameter name="ptr3" class="java.lang.String"/>
		<parameter name="ptr4" class="java.lang.String"/>
		<parameter name="ptr5" class="java.lang.String"/>
		<queryString>
			<![CDATA[]]>
		</queryString>
	</subDataset>
	<parameter name="ptr1" class="java.lang.String"/>
	<parameter name="ptr2" class="java.lang.String"/>
	<parameter name="ptr3" class="java.lang.String"/>
	<parameter name="ptr4" class="java.lang.String"/>
	<parameter name="ptr5" class="java.lang.String"/>
	<parameter name="act1" class="java.lang.String"/>
	<parameter name="act2" class="java.lang.String"/>
	<parameter name="act3" class="java.lang.String"/>
	<parameter name="act4" class="java.lang.String"/>
	<parameter name="act5" class="java.lang.String"/>
	<parameter name="acv1" class="java.lang.String"/>
	<parameter name="acv2" class="java.lang.String"/>
	<parameter name="acv3" class="java.lang.String"/>
	<parameter name="acv4" class="java.lang.String"/>
	<parameter name="acv5" class="java.lang.String"/>
	<parameter name="nct1" class="java.lang.String"/>
	<parameter name="nct2" class="java.lang.String"/>
	<parameter name="nct3" class="java.lang.String"/>
	<parameter name="nct4" class="java.lang.String"/>
	<parameter name="nct5" class="java.lang.String"/>
	<parameter name="ccv1" class="java.lang.String"/>
	<parameter name="ccv2" class="java.lang.String"/>
	<parameter name="ccv3" class="java.lang.String"/>
	<parameter name="ccv4" class="java.lang.String"/>
	<parameter name="ccv5" class="java.lang.String"/>
	<parameter name="ts1" class="java.lang.String"/>
	<parameter name="ts2" class="java.lang.String"/>
	<parameter name="ts3" class="java.lang.String"/>
	<parameter name="ts4" class="java.lang.String"/>
	<parameter name="ts5" class="java.lang.String"/>
	<queryString>
		<![CDATA[]]>
	</queryString>
	<background>
		<band splitType="Stretch"/>
	</background>
	<title>
		<band height="285" splitType="Stretch">
			<componentElement>
				<reportElement positionType="FixRelativeToBottom" x="140" y="50" width="300" height="120" uuid="be80a146-4f33-4d51-a75f-5d3875ba27cd">
					<property name="com.jaspersoft.studio.layout" value="com.jaspersoft.studio.editor.layout.VerticalRowLayout"/>
					<property name="com.jaspersoft.studio.table.style.table_header" value="Table 3_TH"/>
					<property name="com.jaspersoft.studio.table.style.column_header" value="Table 3_CH"/>
					<property name="com.jaspersoft.studio.table.style.detail" value="Table 3_TD"/>
					<property name="com.jaspersoft.studio.unit.width" value="px"/>
					<property name="com.jaspersoft.studio.unit.height" value="px"/>
				</reportElement>
				<jr:table xmlns:jr="http://jasperreports.sourceforge.net/jasperreports/components" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports/components http://jasperreports.sourceforge.net/xsd/components.xsd" whenNoDataType="AllSectionsNoDetail">
					<datasetRun subDataset="Dataset1" uuid="276e54d7-a3bc-4ce6-9b02-1d928df1bf6d">
						<datasetParameter name="ptr3">
							<datasetParameterExpression><![CDATA[$P{ptr3}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ptr4">
							<datasetParameterExpression><![CDATA[$P{ptr4}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="act3">
							<datasetParameterExpression><![CDATA[$P{act3}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="acv4">
							<datasetParameterExpression><![CDATA[$P{acv4}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ptr1">
							<datasetParameterExpression><![CDATA[$P{ptr1}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ptr5">
							<datasetParameterExpression><![CDATA[$P{ptr5}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ptr2">
							<datasetParameterExpression><![CDATA[$P{ptr2}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="act1">
							<datasetParameterExpression><![CDATA[$P{act1}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="act2">
							<datasetParameterExpression><![CDATA[$P{act2}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="act4">
							<datasetParameterExpression><![CDATA[$P{act4}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="act5">
							<datasetParameterExpression><![CDATA[$P{act5}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="acv1">
							<datasetParameterExpression><![CDATA[$P{acv1}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="acv2">
							<datasetParameterExpression><![CDATA[$P{acv2}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="acv3">
							<datasetParameterExpression><![CDATA[$P{acv3}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="acv5">
							<datasetParameterExpression><![CDATA[$P{acv5}]]></datasetParameterExpression>
						</datasetParameter>
					</datasetRun>
					<jr:column width="80" uuid="78a0df97-5b8d-4d1f-8087-f676eeaf3f68">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column1"/>
						<jr:tableHeader style="Table 3_TH" height="30" rowSpan="1">
							<staticText>
								<reportElement x="0" y="0" width="80" height="30" uuid="8d5f09ea-050d-470a-9845-2e9fac75e976"/>
								<textElement textAlignment="Center"/>
								<text><![CDATA[Projected Total Revenue]]></text>
							</staticText>
						</jr:tableHeader>
						<jr:tableFooter style="Table 3_TH" height="30" rowSpan="1">
							<staticText>
								<reportElement mode="Opaque" x="0" y="0" width="80" height="30" forecolor="#241E1D" backcolor="#FCFAFA" uuid="1d4fa987-3be5-4cbb-8bfd-8d6f9414a3f8"/>
								<textElement textAlignment="Center"/>
								<text><![CDATA[$ value  from     ach]]></text>
							</staticText>
						</jr:tableFooter>
						<jr:columnHeader style="Table 3_CH" height="40" rowSpan="1">
							<staticText>
								<reportElement x="0" y="0" width="80" height="40" uuid="6484a593-9063-4a63-bd30-890ad904980d"/>
								<textElement textAlignment="Center"/>
								<text><![CDATA[No of transactions from ach]]></text>
							</staticText>
						</jr:columnHeader>
						<jr:detailCell style="Table 3_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="5be8967d-266b-41d3-ad8b-e0fbf847c617">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column2"/>
						<jr:tableHeader style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="38083d28-2641-4034-877c-8fa91457958f"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ptr1}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement mode="Opaque" x="0" y="0" width="40" height="30" uuid="50354d22-af64-4bb2-8b28-7d95485ae0af"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{acv1}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 3_CH" height="40" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="40" uuid="8e695326-3c19-476c-b93a-beb7f560e586"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{act1}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 3_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="5a9cb2fa-9623-4d7d-ad86-278a8d031d70">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column3"/>
						<jr:tableHeader style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="81121f9c-3beb-4c5b-9b05-2f0702805f4a"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ptr2}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement mode="Opaque" x="0" y="0" width="40" height="30" uuid="ba9e4daf-876a-4800-9286-7239f1502d23"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{acv2}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 3_CH" height="40" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="40" uuid="1ea514b0-1341-45a7-92df-87d126631ae4"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{act2}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 3_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="e62b5094-2e2d-4df9-b3dc-029e258a1419">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column4"/>
						<jr:tableHeader style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="6a08170b-6617-411d-92b4-dec19d2bf183"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ptr3}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement mode="Opaque" x="0" y="0" width="40" height="30" uuid="484ae31b-ab38-4a8c-9a93-a0295b66c388"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{acv3}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 3_CH" height="40" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="40" uuid="51344410-f139-4b92-ad9b-09c67fdc8fa3"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{act3}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 3_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="1c98f11a-b759-4270-8075-e9af206e6f15">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column5"/>
						<jr:tableHeader style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="f925ec16-4c45-4656-a512-ffa8b3ecf448"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ptr4}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement mode="Opaque" x="0" y="0" width="40" height="30" uuid="58017a87-5c79-4e5d-8fd7-09284b3f5000"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{acv4}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 3_CH" height="40" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="40" uuid="828610bf-29b1-4d70-b2d5-b566b617be3a"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{act4}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 3_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="ba488a28-0b52-4fc4-a023-106b01190e56">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column6"/>
						<jr:tableHeader style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="752cbf07-a0c3-4220-b519-81fcf1fc36be"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ptr5}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 3_TH" height="30" rowSpan="1">
							<textField>
								<reportElement mode="Opaque" x="0" y="0" width="40" height="30" uuid="66012fe4-1409-4e22-846f-5cff1fa673fb"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{acv5}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 3_CH" height="40" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="40" uuid="c8cf1741-88ce-49bb-bf0e-901603ad6d89"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{act5}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 3_TD" height="30"/>
					</jr:column>
				</jr:table>
			</componentElement>
			<componentElement>
				<reportElement x="140" y="150" width="290" height="120" uuid="494d9ed6-ed2a-4f51-b27a-38f7913ecf99">
					<property name="com.jaspersoft.studio.layout" value="com.jaspersoft.studio.editor.layout.VerticalRowLayout"/>
					<property name="com.jaspersoft.studio.table.style.table_header" value="Table 5_TH"/>
					<property name="com.jaspersoft.studio.table.style.column_header" value="Table 5_CH"/>
					<property name="com.jaspersoft.studio.table.style.detail" value="Table 5_TD"/>
				</reportElement>
				<jr:table xmlns:jr="http://jasperreports.sourceforge.net/jasperreports/components" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports/components http://jasperreports.sourceforge.net/xsd/components.xsd" whenNoDataType="AllSectionsNoDetail">
					<datasetRun subDataset="Dataset1" uuid="e21395d7-05a9-4f8f-bd86-06f2ef903d89">
						<datasetParameter name="nct1">
							<datasetParameterExpression><![CDATA[$P{nct1}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="nct2">
							<datasetParameterExpression><![CDATA[$P{nct2}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="nct3">
							<datasetParameterExpression><![CDATA[$P{nct3}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="nct4">
							<datasetParameterExpression><![CDATA[$P{nct4}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="nct5">
							<datasetParameterExpression><![CDATA[$P{nct5}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ccv1">
							<datasetParameterExpression><![CDATA[$P{ccv1}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ccv2">
							<datasetParameterExpression><![CDATA[$P{ccv2}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ccv3">
							<datasetParameterExpression><![CDATA[$P{ccv3}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ccv4">
							<datasetParameterExpression><![CDATA[$P{ccv4}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ccv5">
							<datasetParameterExpression><![CDATA[$P{ccv5}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ts1">
							<datasetParameterExpression><![CDATA[$P{ts1}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ts2">
							<datasetParameterExpression><![CDATA[$P{ts2}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ts3">
							<datasetParameterExpression><![CDATA[$P{ts3}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ts4">
							<datasetParameterExpression><![CDATA[$P{ts4}]]></datasetParameterExpression>
						</datasetParameter>
						<datasetParameter name="ts5">
							<datasetParameterExpression><![CDATA[$P{ts5}]]></datasetParameterExpression>
						</datasetParameter>
					</datasetRun>
					<jr:column width="80" uuid="48666b08-df10-4542-9d07-74c8ffe24f8a">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column1"/>
						<jr:tableHeader style="Table 5_TH" height="30" rowSpan="1">
							<staticText>
								<reportElement x="0" y="0" width="80" height="30" uuid="84c963c0-7221-43f8-b836-707df8d00526"/>
								<textElement textAlignment="Center"/>
								<text><![CDATA[No of Transacations from CC]]></text>
							</staticText>
						</jr:tableHeader>
						<jr:tableFooter style="Table 5_TH" height="30" rowSpan="1">
							<staticText>
								<reportElement x="0" y="0" width="80" height="30" uuid="1b627b58-adbb-44e6-9de8-d58ce6ab9633"/>
								<textElement textAlignment="Center"/>
								<text><![CDATA[$ value from other sources]]></text>
							</staticText>
						</jr:tableFooter>
						<jr:columnHeader style="Table 5_CH" height="30" rowSpan="1">
							<staticText>
								<reportElement x="0" y="0" width="80" height="30" uuid="475d402f-3468-4eb7-a346-906af99ae3e2"/>
								<textElement textAlignment="Center" verticalAlignment="Middle"/>
								<text><![CDATA[$ value from CC]]></text>
							</staticText>
						</jr:columnHeader>
						<jr:detailCell style="Table 5_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="360a7f56-c482-43ac-8ea1-1b4e5c21b82f">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column2"/>
						<jr:tableHeader style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="2ce6b71d-887c-430c-a426-7b32c38dba36"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{nct1}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="4251208a-a35c-4db6-93ae-2a0ea2eef970"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ts1}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 5_CH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="26a700f4-07ee-4928-9be1-0ab06e7a18fd"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ccv1}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 5_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="8600967a-b1da-4172-af9c-b39b63ff6d69">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column3"/>
						<jr:tableHeader style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="ebb73040-7008-45af-93e3-32d02c9c625a"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{nct2}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="d4da25bc-3835-453a-85ae-da37562fee45"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ts2}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 5_CH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="fb73bb91-38d1-4486-800d-795fa10dfcbc"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ccv2}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 5_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="f9125c2b-c51c-4dd4-8d92-d083e0b71092">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column4"/>
						<jr:tableHeader style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="1fcae84d-224d-415c-ba36-86c798b91d1e"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{nct3}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="1567aa75-742f-49c1-b61f-b29f39321ed8"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ts3}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 5_CH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="3c39d14a-089f-428f-892f-61814a41939b"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ccv3}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 5_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="b41df634-4c3b-422f-a802-10065183bae4">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column5"/>
						<jr:tableHeader style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="2731fd4b-d9bc-4b90-be3d-005441a87350"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{nct4}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="63d95407-80d7-4c3d-a210-08a35598cbe3"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ts4}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 5_CH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="8756570b-bef7-4445-ba0c-33fd82214763"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ccv4}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 5_TD" height="30"/>
					</jr:column>
					<jr:column width="40" uuid="2828c990-bb60-4e42-8138-7487ae679559">
						<property name="com.jaspersoft.studio.components.table.model.column.name" value="Column6"/>
						<jr:tableHeader style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="90c0d099-fd13-4bdb-9399-439d82ff3502"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{nct5}]]></textFieldExpression>
							</textField>
						</jr:tableHeader>
						<jr:tableFooter style="Table 5_TH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="8ea72645-110a-4b71-aa4c-752aa77d54bc"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ts5}]]></textFieldExpression>
							</textField>
						</jr:tableFooter>
						<jr:columnHeader style="Table 5_CH" height="30" rowSpan="1">
							<textField>
								<reportElement x="0" y="0" width="40" height="30" uuid="f2bd51d6-a408-4197-862e-3a68d7760047"/>
								<textElement textAlignment="Center"/>
								<textFieldExpression><![CDATA[$P{ccv5}]]></textFieldExpression>
							</textField>
						</jr:columnHeader>
						<jr:detailCell style="Table 5_TD" height="30"/>
					</jr:column>
				</jr:table>
			</componentElement>
			<staticText>
				<reportElement x="140" y="20" width="80" height="30" uuid="7bf2a625-3624-4e5d-b874-df26729fb3f2"/>
				<textElement textAlignment="Center" verticalAlignment="Middle"/>
				<text><![CDATA[Metric/Area]]></text>
			</staticText>
			<staticText>
				<reportElement x="210" y="20" width="50" height="30" uuid="50d8b087-f44c-4d9f-b0f6-d4a11a0d74f6"/>
				<textElement textAlignment="Center" verticalAlignment="Middle"/>
				<text><![CDATA[Year1]]></text>
			</staticText>
			<staticText>
				<reportElement x="257" y="20" width="40" height="30" uuid="93e7a99c-f653-4073-868e-d35d353a886c"/>
				<textElement textAlignment="Center" verticalAlignment="Middle"/>
				<text><![CDATA[Year2]]></text>
			</staticText>
			<staticText>
				<reportElement x="300" y="20" width="40" height="30" uuid="2fe8f124-7d83-4f90-8597-c42ca75ceba2"/>
				<textElement textAlignment="Center" verticalAlignment="Middle"/>
				<text><![CDATA[Year3]]></text>
			</staticText>
			<staticText>
				<reportElement x="340" y="20" width="40" height="30" uuid="cd959b6b-0bf0-42cb-af0e-4e960677441b"/>
				<textElement textAlignment="Center" verticalAlignment="Middle"/>
				<text><![CDATA[Year4]]></text>
			</staticText>
			<staticText>
				<reportElement x="380" y="20" width="40" height="30" uuid="680dc698-6cbd-4fa3-a2e5-473040ed63c1"/>
				<textElement textAlignment="Center" verticalAlignment="Middle"/>
				<text><![CDATA[Year5]]></text>
			</staticText>
		</band>
	</title>
	<pageHeader>
		<band height="292" splitType="Stretch"/>
	</pageHeader>
	<columnHeader>
		<band height="126" splitType="Stretch"/>
	</columnHeader>
	<detail>
		<band height="180" splitType="Stretch"/>
	</detail>
	<columnFooter>
		<band height="45" splitType="Stretch"/>
	</columnFooter>
	<pageFooter>
		<band height="54" splitType="Stretch"/>
	</pageFooter>
	<summary>
		<band height="42" splitType="Stretch"/>
	</summary>
</jasperReport>
